<template>
  <div id="app">
    <calculator />
  </div>
</template>

<script>
import calculator from "./components/calculator.vue";

export default {
  name: "app",
  components: {
    calculator
  }
};
</script>

<style>
html {
  height: 100%;
}

body {
  height: 100%;
  display: flex;
}
#app {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
}
</style>
