<template>
  <h1>{{ inputValue }}</h1>
  <input1 @submit="SetinputValue"></input1>
  <div class="border-line"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import input1 from "./input2.vue";

export default defineComponent({
  name: "outputTwo",
  components: { input1 },
  data() {
    return {
      inputValue: "title",
    };
  },
  methods: {
    SetinputValue(a: string) {
      this.inputValue = a;
    },
  },
});
</script>
