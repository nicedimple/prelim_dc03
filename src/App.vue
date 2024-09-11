<template>
  <div id="app">
    <header>
      <h1>Dimple's Chocolate Store</h1>
    </header>
    <main>
      <ItemList />
    </main>
    
  </div>
</template>

<script>
import ItemList from './components/ItemList.vue';

export default {
  name: 'App',
  components: {
    ItemList,
  },
};
</script>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

#app {
  display: flex;
  flex-direction: column;
  align-items: center; 
  }


header {
  padding: 1rem;
  text-align: center;
  background-color: #ccd5ae;
  width: 100%;
}

main {
  padding: 2rem;
  display: flex;
  justify-content: center; 
  width: 100%; 
}

</style>


