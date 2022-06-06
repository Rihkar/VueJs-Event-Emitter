<template>
  <div :style="{ backgroundColor: inputValue }" class="color-box"></div>
  <input4 @change="setInputValue"></input4>
  <div class="border-line"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import input4 from "./input4.vue";

export default defineComponent({
  name: "outputFor",
  components: { input4 },
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
