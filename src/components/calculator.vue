<template>
  <div class="calculator">
    <display :value="valueForDisplay"></display>
    <keyboard @keyboardValue="e => keyboardValue(e.value)" />
  </div>
</template>

<script>
import display from "./display.vue";
import keyboard from "./keyboard.vue";

export default {
  name: "calculator",
  components: {
    display,
    keyboard
  },

  data() {
    return {
      currentNumber: ""
    };
  },

  computed: {
    valueForDisplay() {
      return this.currentNumber.substring(0, 12);
    }
  },

  methods: {
    toNumber(n) {
      return parseInt(n);
    },

    keyboardValue(val) {
      let num = this.toNumber(val);

      if (num) {
        this.currentNumber = this.currentNumber.concat(val).replace(/ /g, "");
      }

      if (val === "AC") {
        this.currentNumber = "";
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.calculator {
  background-color: #eee;
  color: #fff;
  width: 250px;
}
</style>
