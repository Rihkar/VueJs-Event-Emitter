<template>
  <button @click="changeOpacity">change opacity</button>
</template>

<script lang="ts">
import { defineComponent } from "vue";

type opacityLvlType = "1" | "0.5" | "0.1";

export default defineComponent({
  name: "testInputSri",
  emits: ["opacityButtonClick"],
  data() {
    return {
      opacityLvl: "1" as opacityLvlType,
    };
  },
  methods: {
    changeOpacity() {
      if (this.opacityLvl === "1") {
        this.opacityLvl = "0.5";
      } else if (this.opacityLvl === "0.5") {
        this.opacityLvl = "0.1";
      } else {
        this.opacityLvl = "1";
      }
      this.$emit("opacityButtonClick", this.opacityLvl);
    },
  },
});
</script>
