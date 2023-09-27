<script setup>
const year = computed(() => {
  return new Date().getFullYear();
});
</script>

<template>
  <div class="footer">
    <div class="footer-text">&copy; {{ year }} Heather Reynolds</div>
  </div>
</template>

<style lang="scss" scoped>
.footer {
  @apply container mx-auto;
}
.footer-text {
  @apply text-sm py-4 mx-auto border-t border-gray-800;
}
</style>
