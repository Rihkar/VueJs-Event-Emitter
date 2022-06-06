<template>
  <div class="opacity-box" :style="{ opacity: opacityLvl }">
    change my opacity
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "testOutputSri",
  props: ["opacityLvl"],
});
</script>
