<template>
  <testParent1 />
  <testParent2 />
  <testParent3 />
</template>
<script lang="ts">
import { defineComponent } from "vue";
import testParent1 from "@/components/md test/test1/testParent1.vue";
import testParent2 from "@/components/md test/test2/testParent2.vue";
import testParent3 from "@/components/md test/test3/testParent3.vue";

export default defineComponent({
  name: "TestFile",
  components: { testParent1, testParent2, testParent3 },
});
</script>
