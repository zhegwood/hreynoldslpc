<script setup>
const year = computed(() => {
  return new Date().getFullYear();
});
</script>

<template>
  <div class="container mx-auto">
    <div class="text-sm py-4 mx-auto border-t border-gray-800">
      &copy; {{ year }} Heather Reynolds
    </div>
  </div>
</template>
