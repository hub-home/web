<template>
  <div class="card">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
.card {
  width: 100%;
  min-height: 50px;
  border-radius: var(--border-radius);
  background-color: var(--body-lighter);
  border: var(--border);
  padding: 10px 25px;
  transition: background-color 0.3s ease-in-out;
  cursor: pointer;
  user-select: none;

  &:active {
    background-color: var(--hover);
  }
}
</style>
