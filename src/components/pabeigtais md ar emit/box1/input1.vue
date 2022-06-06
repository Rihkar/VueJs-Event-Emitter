<template>
  <form @submit.prevent="submitHandler">
    <input type="text" v-model="inputValue" placeholder="title" />
    <button type="submit">change</button>
  </form>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "inputOne",
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
