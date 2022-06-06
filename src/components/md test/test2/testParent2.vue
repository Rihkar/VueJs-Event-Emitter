<template>
  <testInput2 @inputChange="setInputValue" />
  <testOutput2 :inputValue="inputValue" />
  <div class="border-line"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import testInput2 from "./testInput2.vue";
import testOutput2 from "./testOutput2.vue";
export default defineComponent({
  name: "parentTwo",
  components: {
    testInput2,
    testOutput2,
  },
  data() {
    return {
      inputValue: "bumbieri",
    };
  },
  methods: {
    setInputValue(a: string) {
      this.inputValue = a;
    },
  },
});
</script>
