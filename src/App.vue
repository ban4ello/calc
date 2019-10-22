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
#app {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
