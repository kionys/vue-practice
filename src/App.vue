<script setup>
// import HelloWorld from './components/HelloWorld.vue';
</script>
<script>
export default {
  name: "App",
  data() {
    return {
      menus: ["Home", "Shop", "About"],
      products: [
        { name: "역삼동원룸", value: 50 },
        { name: "천호동원룸", value: 30 },
        { name: "마포구원룸", value: 20 },
      ],
    };
  },
};
</script>

<template>
  <div class="menu">
    <a href="" v-for="(menu, i) in menus" :key="i">{{ menu }}</a>
  </div>
  <ul>
    <li v-for="(product, index) in products" :key="index">{{ product.name }} - {{ product.value }}만원</li>
  </ul>
</template>
<style scoped>
.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
</style>
