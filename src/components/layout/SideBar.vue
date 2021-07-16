<template>
  <div class="sidebar">
    <div class="items">
      <router-link
        v-for="route in $router.options.routes"
        :key="route.path"
        :to="route"
      >
        <Card v-if="!route.meta.hidden" class="item">
          <Icon :name="route.meta.icon" />
          <span>{{ route.name }}</span>
        </Card>
      </router-link>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.sidebar {
  background-color: var(--body-lighter);
  height: 100vh;
  min-width: 275px;
  width: 275px;
  border-right: var(--border);
  padding: var(--gap);

  .items {
    display: flex;
    flex-direction: column;
    gap: var(--gap-small);

    .item {
      display: flex;
      align-items: center;
      gap: 5px;
      transition: all 0.3s ease-in-out;

      &:hover {
        background-color: var(--hover);
      }
    }

    .router-link-active {
      border-radius: var(--border-radius);
      background-color: var(--hover);
    }
  }
}
</style>

<script lang="ts">
import { defineComponent } from "vue";
import Icon from "@/components/base/Icon.vue";
import Card from "@/components/layout/Card.vue";

export default defineComponent({
  name: "SideBar",
  components: {
    Icon,
    Card,
  },
});
</script>
