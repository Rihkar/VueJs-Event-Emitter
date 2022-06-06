<template>
  <input
    @change="submitHandler"
    type="text"
    v-model="inputValue"
    placeholder="title"
  />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "inputTwo",
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
