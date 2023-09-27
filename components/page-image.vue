<template>
  <div class="page-image">
    <slot />
  </div>
</template>

<script>
export default {
  name: "PageImage",
};
</script>

<style lang="scss" scoped>
.page-image {
  @apply flex items-center justify-center;
  ::v-deep(img) {
    @apply border border-gray-800 rounded-lg;
    max-height: 150px;
  }
}
</style>
