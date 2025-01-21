<script setup>
const show_menu = ref(false);
const expanded = ref(false);

const toggleMenu = () => {
  show_menu.value = !show_menu.value;
  expanded.value = false;
};

const onMeetClick = () => {
  expanded.value = true;
};
</script>

<template>
  <div
    class="relative md:hidden bg-gray-100 p-2 text-right border-b border-gray-800"
  >
    <button
      type="button"
      class="h6 w6 inline-flex items-center justify-center p-2 rounded-md text-gray-500 hover:bg-gray-200 border border-black rounded"
      aria-controls="mobile-menu"
      :aria-expanded="show_menu"
      @click="toggleMenu"
    >
      <span class="sr-only">Open main menu</span>
      <svg
        v-if="!show_menu"
        class="h6 w6"
        xmlns="http://www.w3.org/2000/svg"
        fill="black"
        viewBox="0 0 24 24"
        aria-hidden="true"
      >
        <path
          d="M1.5 4.5C1.5 3.67 2.17 3 3 3h18c.83 0 1.5.67 1.5 1.5S21.83 6 21 6H3c-.83 0-1.5-.67-1.5-1.5zm0 7.5c0-.83.67-1.5 1.5-1.5h18c.83 0 1.5.67 1.5 1.5s-.67 1.5-1.5 1.5H3c-.83 0-1.5-.67-1.5-1.5zm21 7.5c0 .83-.67 1.5-1.5 1.5H3c-.83 0-1.5-.67-1.5-1.5S2.17 18 3 18h18c.83 0 1.5.67 1.5 1.5z"
        />
      </svg>
      <svg
        v-else
        xmlns="http://www.w3.org/2000/svg"
        fill="black"
        viewBox="0 0 24 24"
        aria-hidden="true"
      >
        <path
          d="M19.06 7.06a1.502 1.502 0 00-2.124-2.124L12 9.876 7.06 4.942a1.502 1.502 0 00-2.124 2.123L9.876 12l-4.935 4.94a1.502 1.502 0 002.123 2.124L12 14.124l4.94 4.935a1.502 1.502 0 002.124-2.123L14.124 12z"
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
      <ul
        v-if="show_menu"
        class="absolute w-full top-14 right-0 left-0 bg-gray-100 border-b border-gray-800 z-50"
      >
        <li class="py-2 px-4 hover:bg-gray-200">
          <NuxtLink to="/" @click="toggleMenu"> Welcome </NuxtLink>
        </li>
        <li class="py-2 px-4 hover:bg-gray-200">
          <!--
          <NuxtLink to="/the-team" @click="toggleMenu"> Meet the Team</NuxtLink>
          -->
          <button class="text-right" @click="onMeetClick">
            Meet the Team
            <ul v-if="expanded" class="mt-2">
              <li class="py-2 hover:bg-gray-200">
                <NuxtLink to="/heather-reynolds" @click="toggleMenu">
                  Heather Reynolds, MA, LPC, CHt, CRRTS
                </NuxtLink>
              </li>
              <li class="py-2 hover:bg-gray-200">
                <NuxtLink to="/julie-maerz" @click="toggleMenu">
                  Julie Maerz, MA, LPC
                </NuxtLink>
              </li>
            </ul>
          </button>
        </li>
        <li class="py-2 px-4 hover:bg-gray-200">
          <NuxtLink to="/rapid-resolution-therapy" @click="toggleMenu">
            Rapid Resolution Therapy
          </NuxtLink>
        </li>
        <li class="py-2 px-4 hover:bg-gray-200">
          <NuxtLink to="/neuroptimal-neurofeedback" @click="toggleMenu">
            NeurOptimal<sup>&reg;</sup> Neurofeedback
          </NuxtLink>
        </li>
        <li class="py-2 px-4 hover:bg-gray-200">
          <NuxtLink to="/testimonials" @click="toggleMenu">
            Testimonials
          </NuxtLink>
        </li>
        <li class="py-2 px-4 hover:bg-gray-200">
          <NuxtLink to="/faq" @click="toggleMenu"> FAQ </NuxtLink>
        </li>
        <li class="py-2 px-4 hover:bg-gray-200">
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
