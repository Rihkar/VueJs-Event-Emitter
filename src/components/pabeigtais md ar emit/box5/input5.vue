<template>
  <form @submit.prevent="submitHandler">
    <input type="text" v-model="inputValue" placeholder="title" />
    <button type="submit">change</button>
  </form>
  <form @submit.prevent="secondSubmitHandler">
    <input type="text" v-model="secondInputValue" placeholder="description" />
    <button type="submit">change</button>
  </form>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "inputOne",
  emits: ["submit", "secondSubmit"],
  data() {
    return {
      inputValue: "",
      secondInputValue: "",
    };
  },
  methods: {
    submitHandler() {
      this.$emit("submit", this.inputValue);

      this.inputValue = "";
    },
    secondSubmitHandler() {
      this.$emit("secondSubmit", this.secondInputValue);

      this.secondInputValue = "";
    },
  },
});
</script>
