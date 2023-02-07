<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { ref, reactive } from "vue";
import colorPicks from "../composables/colorPicks";

export default {
  setup() {
      const colorManager = ref("")

    const {colors, message, matchColor} = colorPicks();

    return { colors, message, matchColor };
  },
};
</script>

<style></style>
