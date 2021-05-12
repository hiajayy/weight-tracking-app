<template>
  <the-header></the-header>
  <the-weight></the-weight>
</template>

<script>
import TheHeader from "./components/layout/TheHeader";
import TheWeight from "./components/TheWeight";
export default {
  name: "App",

  components: {
    TheHeader,
    TheWeight,
  },
};
</script>

<style>
:root {
  --primary-color: #98ddca;
  --secondary-color: #d5ecc2;
  --orange-color: #ffd3b4;
  --pink-color: #ffaaa7;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  font-family: "Jost", sans-serif;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
}
</style>
