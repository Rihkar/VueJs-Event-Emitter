<template>
  <h1>{{ `man negarso ${inputValue}` }}</h1>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "testOutputTwo",
  props: ["inputValue"],
});
</script>
