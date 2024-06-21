<template>
  <div class="container">
    <div class="row">
        <h2>Friends</h2>
        <Friends/> 
    </div>
    <div class="row">
        <h2>Products</h2>
        <Products/>
    </div>
  </div>
</template>

<script>
import Friends from "@/components/Friends";
import Products from "@/components/Products.vue";
export default {
    name: "App",
    components: {
        Friends,
        Products,
    },
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

}
</style>