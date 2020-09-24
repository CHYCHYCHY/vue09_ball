<template>
  <container>
    <Ball></Ball>
  </container>
</template>

<script>
import Ball from "./components/Ball";
export default {
  name: "App",
  // eslint-disable-next-line vue/no-unused-components
  components: { Ball },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
