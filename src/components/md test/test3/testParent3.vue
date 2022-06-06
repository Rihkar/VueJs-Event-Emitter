<template>
  <testInput3 @opacityButtonClick="setOpacityValue" />
  <testOutput3 :opacityLvl="opacitylvl" />
  <div class="border-line"></div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import testInput3 from "./testInput3.vue";
import testOutput3 from "./testOutput3.vue";

export default defineComponent({
  name: "parentSri",
  components: {
    testInput3,
    testOutput3,
  },
  data() {
    return {
      opacitylvl: "1",
    };
  },
  methods: {
    setOpacityValue(a: string) {
      this.opacitylvl = a;
    },
  },
});
</script>
