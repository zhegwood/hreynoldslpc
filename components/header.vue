<template>
  <div class="header">
    <div class="flex flex-auto container mx-auto p-2">
      <div class="flex-none">
        <img
          src="~/assets/images/logo.jpg"
          alt="Heather Reynolds Logo"
          class="bordered-image block w-40 sm:w-48 md:w-56 lg:w-64"
        />
      </div>
      <div class="credentials grow text-center text-white">
        <p class="text-sm sm:text-xl md:text-3xl lg:text-4xl mb-4 font-normal">
          Heather Reynolds, <br />MA, LPC, CHt, CRRTS
        </p>
        <p class="text-xs sm:text-lg md:text-2xl lg:text-3xl mb-2 font-normal">
          Licensed Professional Counselor
        </p>
        <p class="text-xs sm:text-lg md:text-2xl lg:text-3xl mb-2 font-normal">
          Certified Rapid Resolution<br />
          Therapy Specialist
        </p>
        <p class="text-xs sm:text-base md:text-lg lg:text-2xl font-normal">
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
.logo {
  border-color: #2d5581;
}
.credentials {
  min-width: 200px;
}
</style>
