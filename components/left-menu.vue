<script setup>
const expanded = ref(false);

const onMeetClick = () => {
  expanded.value = !expanded.value;
};
</script>
<template>
  <div class="left-menu">
    <div class="left-menu-inner rounded-xl mt-2 mb-8 p-4 pt-8">
      <ul class="mb-5">
        <li>
          <NuxtLink
            to="/"
            class="block text-sm rounded mb-0.5 px-4 py-2 bg-gray-100 hover:cursor-pointer hover:bg-gray-200"
            @click="expanded = false"
          >
            Welcome
          </NuxtLink>
        </li>
        <li>
          <!--
          <NuxtLink
            to="/the-team"
            class="block text-sm rounded mb-0.5 px-4 py-2 bg-gray-100 hover:cursor-pointer hover:bg-gray-200"
          >
            Meet the team
          </NuxtLink>
          -->
          <button
            class="block text-sm rounded mb-0.5 px-4 py-2 bg-gray-100 hover:cursor-pointer text-left w-full"
            :class="{ 'hover:bg-gray-200': !expanded }"
            @click="onMeetClick"
          >
            Meet the Team
            <ul v-if="expanded">
              <li>
                <NuxtLink
                  to="/heather-reynolds"
                  class="block text-sm rounded mb-0.5 px-4 py-2 bg-gray-100 hover:cursor-pointer hover:bg-gray-200"
                >
                  Heather Reynolds, MA, LPC, CHt, CRRTS
                </NuxtLink>
              </li>
              <li>
                <NuxtLink
                  to="/julie-maerz"
                  class="block text-sm rounded mb-0.5 px-4 py-2 bg-gray-100 hover:cursor-pointer hover:bg-gray-200"
                >
                  Julie Maerz, MA, LPC
                </NuxtLink>
              </li>
            </ul>
          </button>
        </li>
        <li>
          <NuxtLink
            to="/rapid-resolution-therapy"
            class="block text-sm rounded mb-0.5 px-4 py-2 bg-gray-100 hover:cursor-pointer hover:bg-gray-200"
            @click="expanded = false"
          >
            Rapid Resolution Therapy
          </NuxtLink>
        </li>
        <li>
          <NuxtLink
            to="/neuroptimal-neurofeedback"
            class="block text-sm rounded mb-0.5 px-4 py-2 bg-gray-100 hover:cursor-pointer hover:bg-gray-200"
            @click="expanded = false"
          >
            NeurOptimal<sup>&reg;</sup> Neurofeedback
          </NuxtLink>
        </li>
        <li>
          <NuxtLink
            to="/testimonials"
            class="block text-sm rounded mb-0.5 px-4 py-2 bg-gray-100 hover:cursor-pointer hover:bg-gray-200"
            @click="expanded = false"
          >
            Testimonials
          </NuxtLink>
        </li>
        <li>
          <NuxtLink
            to="/faq"
            class="block text-sm rounded mb-0.5 px-4 py-2 bg-gray-100 hover:cursor-pointer hover:bg-gray-200"
            @click="expanded = false"
          >
            FAQ
          </NuxtLink>
        </li>
      </ul>
      <div class="mb-5">
        <a
          href="https://www.zocdoc.com/practice/heather-reynolds-ma-lpc-58322"
          target="_blank"
          class="zd-plugin"
          data-type="book-button"
          data-practice-id="58322"
        >
          <img
            src="https://offsiteSchedule.zocdoc.com/images/remote/rb_BookAnAppt_White_214x74.png"
            alt="Book an Appointment"
            class="h-14 mx-auto"
            style="border: 0"
          />
        </a>
      </div>
    </div>
    <a href="https://www.facebook.com/denverrapidresolution" target="_blank">
      <img
        src="~/assets/images/facebook.png"
        alt="Reach Us on Facebook"
        class="h-10 w-10 mx-auto"
      />
    </a>
  </div>
</template>

<style lang="scss" scoped>
.left-menu-inner {
  background-color: #658aac;
}
.router-link-exact-active {
  @apply bg-gray-200;
}
</style>
