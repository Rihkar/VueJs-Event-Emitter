<template>
  <testInput1 @inputChange="setInputValue" />
  <testOutput1 :inputValue="inputValue" />
  <div class="border-line"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import testInput1 from "./testInput1.vue";
import testOutput1 from "./testOutput1.vue";
export default defineComponent({
  name: "parentOne",
  components: {
    testInput1,
    testOutput1,
  },
  data() {
    return {
      inputValue: "aboli",
    };
  },
  methods: {
    setInputValue(a: string) {
      this.inputValue = a;
    },
  },
});
</script>
