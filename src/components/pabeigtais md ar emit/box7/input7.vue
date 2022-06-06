<template>
  Toggle square invisibility on button click.
  <button @click="submitHandler">toggle</button>
</template>

<script lang="ts">
import { defineComponent } from "vue";

type VisibilityType = "visible" | "hidden";

export default defineComponent({
  name: "inputSev",
  emits: ["toggle"],
  data() {
    return {
      boxVisibility: "visible" as VisibilityType,
    };
  },
  methods: {
    submitHandler() {
      this.$emit("toggle", this.boxVisibility);
    },
  },
});
</script>
