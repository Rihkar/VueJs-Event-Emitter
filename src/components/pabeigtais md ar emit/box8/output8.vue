<template>
  <div :style="{ visibility: boxVisibility }" class="golden-box"></div>
  <input8 @toggle="toggleVisibility"></input8>
  <div class="border-line"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import input8 from "./input8.vue";

type VisibilityType = "visible" | "hidden";

export default defineComponent({
  name: "outputEit",
  components: { input8 },
  data() {
    return {
      boxVisibility: "visible" as VisibilityType,
    };
  },
  methods: {
    toggleVisibility() {
      if (this.boxVisibility === "visible") {
        return (this.boxVisibility = "hidden");
      } else {
        return (this.boxVisibility = "visible");
      }
    },
  },
});
</script>
