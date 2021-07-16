<template>
  <img :src="`/static/icons/${name}.svg`" class="icon" />
</template>

<style lang="scss" scoped>
.icon {
  width: 24px;
}
</style>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Icon",
  props: {
    name: {
      type: String,
    },
  },
});
</script>
