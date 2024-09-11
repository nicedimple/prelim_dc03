<template>
  <div class="item" v-if="item.isVisible">
    <p class="item-details">{{ item.name }} - ₱{{ item.price }}</p>
    <button class="add-to-cart-button" @click="addToCart">Add to Cart</button>
  </div>
</template>

<script>
export default {
  props: ['item'],
  methods: {
    addToCart() {
      this.$emit('add-to-cart', this.item);
    },
  },
};
</script>

<style scoped>
.item {
  border: 1px solid #ddd;
  border-radius: 5px;
  padding: 16px;
  margin-bottom: 16px;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: background-color 0.3s, box-shadow 0.3s;
}

.item:hover {
  background-color: #f9f9f9;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.item-details {
  font-size: 16px;
  margin: 0;
  color: #333;
}

.add-to-cart-button {
  background-color: #606c38;
  color: #fff;
  border: none;
  padding: 8px 16px;
  border-radius: 4px;
  cursor: pointer;
  font-size: 14px;
  transition: background-color 0.2s;
}

.add-to-cart-button:hover {
  background-color: #283618;
}
</style>
