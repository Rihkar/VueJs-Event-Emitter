<template>
  <form @submit.prevent="inputChange" action="">
    <input v-model="inputValue" type="text" placeholder="man negarso..." />
    <button>add</button>
  </form>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "testInputTwo",
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
