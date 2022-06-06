<template>
  <h1>{{ titleValue }}</h1>
  <h1>{{ descriptionValue }}</h1>

  <input6 @submit="setInputValue" @secondSubmit="setDescriptionValue"></input6>
  <div class="border-line"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import input6 from "./input6.vue";

export default defineComponent({
  name: "outputFiv",
  components: { input6 },
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
