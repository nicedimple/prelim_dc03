<template>
  <div class="item-list">
    <Item
      v-for="item in filteredItems"
      :key="item.name"
      :item="item"
      @add-to-cart="handleAddToCart"
    />
  </div>
</template>

<script>
import Item from './Item.vue';

export default {
  name: 'ItemList',
  components: {
    Item,
  },
  data() {
    return {
      items: [
        { name: 'Kitkat', price: 30, isVisible: true },
        { name: 'Toblerone', price: 70, isVisible: true },
        { name: 'Snickers', price: 50, isVisible: true },
        { name: 'Bounty', price: 45, isVisible: true },
      ],
    };
  },
  computed: {
    filteredItems() {
      return this.items.filter(item => item.isVisible);
    },
  },
  methods: {
    handleAddToCart(item) {
      console.log('Added to Cart:', item.name, item.price);
    },
  },
};
</script>

<style scoped>
.item-list {
  display: flex;
  flex-direction: column;
  padding: 16px;
}

.item-list .item {
  margin: 8px 0;
}
</style>
