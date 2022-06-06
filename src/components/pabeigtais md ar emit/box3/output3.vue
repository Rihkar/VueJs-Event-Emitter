<template>
  <div :style="{ backgroundColor: inputValue }" class="color-box"></div>
  <input3 @submit="setInputValue"></input3>
  <div class="border-line"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import input3 from "./input3.vue";

export default defineComponent({
  name: "outputSri",
  components: { input3 },
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
