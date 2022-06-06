<template>
  <div :style="{ visibility: boxVisibility }" class="golden-box"></div>
  <input7 @toggle="toggleVisibility"></input7>
  <div class="border-line"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import input7 from "./input7.vue";

type VisibilityType = "visible" | "hidden";

export default defineComponent({
  name: "outputSev",
  components: { input7 },
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
