<template>
  <div class="h-screen">
    <Header />
    <MobileMenu class="mobile-menu" />
    <div class="full-content">
      <div class="full-content-inner">
        <LeftMenu class="left-menu" />
        <div class="page-content">
          <slot />
          <PageFooter />
        </div>
      </div>
      <Footer />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.mobile-menu {
  @apply block sm:hidden;
}
.full-content {
  @apply flex flex-col container mx-auto px-2 pt-4;
}
.full-content-inner {
  @apply flex flex-row;
}
.page-content {
  @apply grow sm:ml-8;
}
.left-menu {
  @apply hidden sm:block flex-none w-40 md:w-56 lg:w-64;
}
</style>
