<template>
  <h1>{{ `man garso ${inputValue}` }}</h1>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "testOutputOne",
  props: ["inputValue"],
});
</script>
