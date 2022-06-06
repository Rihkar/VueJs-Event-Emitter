<template>
  <h1>{{ inputValue }}</h1>
  <input1 @submit="setInputValue"></input1>
  <div class="border-line"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import input1 from "./input1.vue";

export default defineComponent({
  name: "outputOne",
  components: { input1 },
  data() {
    return {
      inputValue: "title",
    };
  },
  methods: {
    setInputValue(a: string) {
      this.inputValue = a;
    },
  },
});
</script>
