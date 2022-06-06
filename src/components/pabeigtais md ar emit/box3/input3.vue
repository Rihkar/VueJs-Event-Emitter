<template>
  <form @submit.prevent="submitHandler">
    <input type="text" v-model="inputValue" placeholder="type a color" />
    <button type="submit">change</button>
  </form>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "inputSri",
  emits: ["submit"],
  data() {
    return {
      inputValue: "",
    };
  },
  methods: {
    submitHandler() {
      this.$emit("submit", this.inputValue);
      this.inputValue = "";
    },
  },
});
</script>
