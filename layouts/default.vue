<script setup>
useHead({
  htmlAttrs: {
    lang: "en",
  },
  meta: [
    {
      name: "description",
      content:
        "Heather Reynolds, MA, LPC, CHt, CRRTS. Licensed Professional Counselor. Certified Rapid Resolution Therapy Specialist.",
    },
  ],
});
onBeforeMount(() => {
  let script = document.createElement("script");
  script.type = "text/javascript";
  script.async = true;
  script.src = "//offsiteschedule.zocdoc.com/plugin/embed";
  document.body.appendChild(script);
});
</script>
<template>
  <div class="h-screen">
    <Header />
    <MobileMenu class="block sm:hidden" />
    <div class="flex flex-col container mx-auto px-2 pt-4">
      <div class="flex flex-row">
        <LeftMenu class="hidden sm:block flex-none w-40 md:w-56 lg:w-64" />
        <div class="grow sm:ml-8">
          <slot />
          <PageFooter />
        </div>
      </div>
      <Footer />
    </div>
  </div>
</template>
