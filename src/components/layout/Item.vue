<template>
  <Card class="item">
    <Icon :name="icon" />
    <div class="info">
      <h3>{{ title }}</h3>
      <p class="desc">{{ description }}</p>
    </div>
    <Icon name="keyboard_arrow_right" />
  </Card>
</template>

<style lang="scss" scoped>
.item {
  display: flex;
  gap: var(--gap);

  .info {
    width: 100%;
    text-overflow: ellipsis;
    overflow: hidden;
    white-space: nowrap;

    .desc {
      color: var(--text-secundair);
    }
  }
}
</style>

<script lang="ts">
import { defineComponent } from "vue";
import Card from "@/components/layout/Card.vue";
import Icon from "@/components/base/Icon.vue";

export default defineComponent({
  name: "Item",
  components: {
    Card,
    Icon,
  },
  props: {
    icon: {
      type: String,
    },
    title: {
      type: String,
    },
    description: {
      type: String,
    },
  },
});
</script>
