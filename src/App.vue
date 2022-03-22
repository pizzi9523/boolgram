<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <header>
      <Nav />
    </header>
    <!-- /header  -->

    <main></main>
    <!-- /main  -->

    <footer></footer>
    <!-- /footer  -->
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Nav from "./components/Nav.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    Nav,
  },
};
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap.scss";
</style>
