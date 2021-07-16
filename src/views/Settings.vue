<template>
  <div class="layout">
    <SideBar />
    <main class="content">
      <ColumnLayout>
        <Column>
          <h1>Configure Hubhome</h1>
          <p class="desc">
            Hier kun je componenten en Hubhome configureren. Het is nog niet
            mogelijk om alles te configureren via de ui, maar we werken eraan.
          </p>
        </Column>
        <Column>
          <ListLayout>
            <Item
              icon="dashboard"
              title="Apparaten"
              description="Beheer en configueer apparaten"
            />
            <Item
              icon="dashboard"
              title="Gebieden"
              description="Groepeer apparaten in gebieden"
            />
            <Item
              icon="dashboard"
              title="Apparaten"
              description="Beheer en configueer apparaten"
            />
          </ListLayout>
        </Column>
      </ColumnLayout>
    </main>
  </div>
</template>

<style lang="scss" scoped>
.layout {
  display: flex;

  .content {
    width: 60%;
    margin: 0 auto;
    padding: var(--gap-large);

    .desc {
      color: var(--text-secundair);
    }
  }
}
</style>

<script lang="ts">
import { defineComponent } from "vue";
import SideBar from "@/components/layout/SideBar.vue";
import ColumnLayout from "@/components/layout/ColumnLayout.vue";
import Column from "@/components/layout/Column.vue";
import Item from "@/components/layout/Item.vue";
import ListLayout from "@/components/layout/ListLayout.vue";

export default defineComponent({
  name: "Settings",
  components: {
    SideBar,
    ColumnLayout,
    Column,
    Item,
    ListLayout,
  },
});
</script>
