<script setup>
const show_menu = ref(false);

const toggleMenu = () => {
  show_menu.value = !show_menu.value;
};
</script>

<template>
  <div class="mobile-menu">
    <button
      type="button"
      class="mobile-menu-button"
      aria-controls="mobile-menu"
      aria-expanded="false"
      @click="toggleMenu"
    >
      <span class="sr-only">Open main menu</span>
      <svg
        v-if="!show_menu"
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        aria-hidden="true"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M4 6h16M4 12h16M4 18h16"
        />
      </svg>
      <svg
        v-else
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        aria-hidden="true"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M6 18L18 6M6 6l12 12"
        />
      </svg>
    </button>
    <transition
      enter-active-class="transition ease-in duration-100"
      enter-from-class="transform opacity-0 scale-75"
      enter-to-class="transform opacity-100 scale-100"
      leave-active-class="transition ease-in duration-100"
      leave-from-class="transform opacity-100 scale-100"
      leave-to-class="transform opacity-0 scale-75"
    >
      <ul v-if="show_menu" class="menu-container">
        <li class="menu-item">
          <NuxtLink to="/" @click="toggleMenu"> Welcome </NuxtLink>
        </li>
        <li class="menu-item">
          <NuxtLink to="/about-me" @click="toggleMenu"> About </NuxtLink>
        </li>
        <li class="menu-item">
          <NuxtLink to="/rapid-resolution-therapy" @click="toggleMenu">
            Rapid Resolution Therapy
          </NuxtLink>
        </li>
        <li class="menu-item">
          <NuxtLink to="/neuroptimal-neurofeedback" @click="toggleMenu">
            NeurOptimal<sup>&reg;</sup> Neurofeedback
          </NuxtLink>
        </li>

        <li class="menu-item">
          <NuxtLink to="/testimonials" @click="toggleMenu">
            Testimonials
          </NuxtLink>
        </li>
        <li class="menu-item">
          <NuxtLink to="/faq" @click="toggleMenu"> FAQ </NuxtLink>
        </li>
        <li class="menu-item">
          <a
            href="http://www.zocdoc.com/practice/heather-reynolds-ma-lpc-58322"
            target="_blank"
            class="zd-plugin"
            data-type="book-button"
            data-practice-id="58322"
          >
            Book an Appointment
          </a>
        </li>
      </ul>
    </transition>
  </div>
</template>

<style lang="scss" scoped>
.mobile-menu {
  @apply relative md:hidden bg-gray-100 p-2 text-right border-b border-gray-800;
}
.mobile-menu-button {
  @apply inline-flex items-center justify-center p-2 rounded-md text-gray-500 hover:bg-gray-200;
  svg {
    @apply h-6 w-6;
  }
}
.menu-container {
  @apply absolute w-full top-14 right-0 left-0 bg-gray-100 border-b border-gray-800;
}
.menu-item {
  @apply py-2 px-4 hover:bg-gray-200;
}
</style>
