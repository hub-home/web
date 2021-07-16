<template>
  <SideBar />
  <h1>Hello World</h1>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import SideBar from "@/components/layout/SideBar.vue";

export default defineComponent({
  name: "Dashboard",
  components: {
    SideBar,
  },
});
</script>
