<template>
  <input
    @change="inputChange"
    v-model="inputValue"
    type="text"
    placeholder="man garso..."
  />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "testInputOne",
  emits: ["inputChange"],
  data() {
    return {
      inputValue: "",
    };
  },
  methods: {
    inputChange() {
      this.$emit("inputChange", this.inputValue);
      this.inputValue = "";
    },
  },
});
</script>
