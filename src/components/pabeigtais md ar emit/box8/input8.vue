<template>
  Toggle square invisibility on checkbox click.
  <input type="checkbox" @click="submitHandler" />
</template>

<script lang="ts">
import { defineComponent } from "vue";

type VisibilityType = "visible" | "hidden";

export default defineComponent({
  name: "inputEit",
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
