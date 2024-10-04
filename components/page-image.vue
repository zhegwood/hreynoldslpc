<template>
  <div class="page-image flex items-center justify-center">
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
  ::v-deep(img) {
    @apply border border-gray-800 rounded-lg;
    max-height: 150px;
  }
}
</style>
