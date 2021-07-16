<template>
  <div class="columns">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
.columns {
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  gap: var(--gap);
}
</style>
