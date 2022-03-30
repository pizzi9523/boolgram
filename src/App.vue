<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <header>
      <Nav />
    </header>
    <!-- /header  -->

    <main>
      <Main />
    </main>
    <!-- /main  -->

    <footer></footer>
    <!-- /footer  -->
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Nav from "./components/Nav.vue";
import Main from "./components/Main.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    Nav,
    Main,
  },
};
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap.scss";

header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  background-color: white;
}

main {
  margin-top: 86px;
}
</style>
