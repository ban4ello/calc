<template>
  <div class="calculator">
    <display :value="123456789012345678"></display>
  </div>
</template>

<script>
import display from "./display.vue";

export default {
  name: "calculator",

  components: {
    display
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.calculator {
  background-color: #eee;
  color: #fff;
  width: 250px;
  height: 300px;
}
</style>
