<template>
  <output1 />
  <output2 />
  <output3 />
  <output4 />
  <output5 />
  <output6 />
  <output7 />
  <output8 />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import output1 from "../components/pabeigtais md ar emit/box1/input1.vue";
import output2 from "../components/pabeigtais md ar emit/box2/output2.vue";
import output3 from "../components/pabeigtais md ar emit/box3/output3.vue";
import output4 from "../components/pabeigtais md ar emit/box4/output4.vue";
import output5 from "../components/pabeigtais md ar emit/box5/output5.vue";
import output6 from "../components/pabeigtais md ar emit/box6/output6.vue";
import output7 from "../components/pabeigtais md ar emit/box7/output7.vue";
import output8 from "../components/pabeigtais md ar emit/box8/output8.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    output1,
    output2,
    output3,
    output4,
    output5,
    output6,
    output7,
    output8,
  },
});
</script>
