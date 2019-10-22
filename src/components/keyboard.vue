<template>
  <div class="keyboard">
    <button
      class="keyboard-btn"
      @click="update"
      v-for="(btn, i) in btns"
      :key="i"
    >
      {{ btn }}
    </button>
  </div>
</template>

<script>
export default {
  props: {},

  data() {
    return {
      btns: [
        "AC",
        "+/-",
        "%",
        "/",
        "7",
        "8",
        "9",
        "*",
        "4",
        "5",
        "6",
        "-",
        "1",
        "2",
        "3",
        "+",
        "0",
        ",",
        "="
      ]
    };
  },

  computed: {},

  methods: {
    update(e) {
      this.$emit("keyboardValue", { value: e.target.textContent });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.keyboard {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(5, 1fr);
  justify-items: center;

  .keyboard-btn {
    font-size: 20px;
    width: 50px;
    height: 50px;
  }
}
</style>
