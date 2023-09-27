<template>
  <div class="header">
    <div class="header-inner">
      <div class="logo-container">
        <img
          src="~/assets/images/logo.jpg"
          alt="Heather Reynolds Logo"
          class="logo bordered-image"
        />
      </div>
      <div class="credentials">
        <p class="heading-1">Heather Reynolds, <br />MA, LPC, CHt, CRRTS</p>
        <p class="heading-2">Licensed Professional Counselor</p>
        <p class="heading-2">
          Certified Rapid Resolution<br />
          Therapy Specialist
        </p>
        <p class="heading-3">
          Sessions available in person and via secure telehealth<br />
          Now offering NeurOptimal<sup>&reg;</sup> Neurofeedback!
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.header {
  background-color: #658aac;
}
.header-inner {
  @apply flex flex-auto container mx-auto p-2;
}
.logo-container {
  @apply flex-none;
}
.logo {
  @apply block w-40 sm:w-48 md:w-56 lg:w-64;
  border-color: #2d5581;
}
.credentials {
  @apply grow text-center text-white;
  min-width: 200px;
}
.heading-1 {
  @apply text-sm sm:text-xl md:text-3xl lg:text-4xl mb-4 font-normal;
}
.heading-2 {
  @apply text-xs sm:text-lg md:text-2xl lg:text-3xl mb-2 font-normal;
}
.heading-3 {
  @apply text-xs sm:text-base md:text-lg lg:text-2xl font-normal;
}
</style>
