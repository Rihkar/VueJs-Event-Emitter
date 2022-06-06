<template>
  <input
    type="text"
    v-model="inputValue"
    @change="submitHandler"
    placeholder="title"
  />
  <br />
  <input
    type="text"
    v-model="secondInputValue"
    @change="secondSubmitHandler"
    placeholder="description"
  />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "inputFiv",
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
