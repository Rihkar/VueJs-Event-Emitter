<template>
  <input
    @change="submitHandler"
    type="text"
    v-model="inputValue"
    placeholder="type a color"
  />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "inputFor",
  emits: ["change"],
  data() {
    return {
      inputValue: "",
    };
  },
  methods: {
    submitHandler() {
      this.$emit("change", this.inputValue);
      this.inputValue = "";
    },
  },
});
</script>
