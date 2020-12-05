<template>
  <div id="app">
    <HelloWorld :images="images" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

const data = [
  require("./assets/photo-1458302488426-c9fe676e00b0.jpg"),
  require("./assets/photo-1517842512476-c5a491eb1cf6.jpg"),
  require("./assets/photo-1438183972690-6d4658e3290e.jpg"),
  require("./assets/photo-1534297169727-a78dc2d3dea4.jpg"),
  require("./assets/photo-1474366521946-c3d4b507abf2.jpg"),
  require("./assets/photo-1505063111741-9b87489f9bd7.jpg"),
  require("./assets/photo-1531137199527-9546e8290fd4.jpg"),
  require("./assets/photo-1520699049698-acd2fccb8cc8.jpg"),
  require("./assets/photo-1519682337058-a94d519337bc.jpg"),
];

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data: () => {
    return {
      images: data,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: rgb(243, 243, 243);
  align-content: center;
  display: flex;
}
</style>
