<template>
  <h1>{{ titleValue }}</h1>
  <h1>{{ descriptionValue }}</h1>

  <input5 @submit="setInputValue" @secondSubmit="setDescriptionValue"></input5>
  <div class="border-line"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import input5 from "./input5.vue";

export default defineComponent({
  name: "outputOne",
  components: { input5 },
  data() {
    return {
      titleValue: "title",
      descriptionValue: "description",
    };
  },
  methods: {
    setInputValue(a: string) {
      this.titleValue = a;
    },
    setDescriptionValue(a: string) {
      this.descriptionValue = a;
    },
  },
});
</script>
