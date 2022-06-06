<template>
  <testInputOne></testInputOne>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import testInputOne from "./input1.vue";

export default defineComponent({
  name: "parentOne",
  components: {
    testInputOne,
  },
});
</script>
