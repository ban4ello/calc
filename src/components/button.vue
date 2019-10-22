<template>
  <div class="display">
    <span>{{ val }}</span>
  </div>
</template>

<script>
export default {
  props: {
    value: Number
  },

  computed: {
    val() {
      if (this.value) {
        return String(this.value).substring(0, 12);
      } else {
        return "0";
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.display {
  background-color: #4c4c4c;
  font-size: 30px;
  text-align: right;
  padding: 20px;
}
</style>
