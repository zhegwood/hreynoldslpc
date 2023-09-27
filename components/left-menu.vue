<template>
  <div class="left-menu">
    <div class="left-menu-inner">
      <ul class="mb-5">
        <li>
          <NuxtLink to="/" class="menu-link"> Welcome </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about-me" class="menu-link"> About </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/rapid-resolution-therapy" class="menu-link">
            Rapid Resolution Therapy
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/neuroptimal-neurofeedback" class="menu-link">
            NeurOptimal<sup>&reg;</sup> Neurofeedback
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/testimonials" class="menu-link">
            Testimonials
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/faq" class="menu-link"> FAQ </NuxtLink>
        </li>
      </ul>
      <div class="image-container">
        <div class="image-book">
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
              style="border: 0"
            />
          </a>
        </div>
      </div>
      <img src="~/assets/images/rrt_logo.png" alt="Rapid Resolution Therapy" />
    </div>
    <img
      src="~/assets/images/certificate.png"
      alt="Certified Practitioner"
      class="image-cert"
    />
    <a href="https://www.facebook.com/denverrapidresolution" target="_blank">
      <img
        src="~/assets/images/facebook.png"
        alt="Reach Us on Facebook"
        class="fb-img"
      />
    </a>
  </div>
</template>

<style lang="scss" scoped>
.left-menu-inner {
  background-color: #658aac;
  @apply rounded-xl mt-2 mb-8 p-4 pt-8;
}
.menu-link {
  @apply block text-sm rounded mb-0.5 px-4 py-2 bg-gray-100 hover:cursor-pointer hover:bg-gray-200;
}
.menu-link.router-link-exact-active {
  @apply bg-gray-200;
}
.image-container {
  @apply mb-5;
}
.image-book {
  img {
    @apply h-14 mx-auto;
  }
}
.image-cert {
  @apply mx-auto mb-8;
}
.fb-img {
  @apply h-10 mx-auto;
}
</style>
