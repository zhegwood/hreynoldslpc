<template>
  <h1 class="h1 mb-8">About Me</h1>
  <page-image class="mb-8">
    <img src="~/assets/images/heather.png" alt="Heather Reynolds" />
  </page-image>
  <div class="about-container">
    <ul class="list">
      <li class="text mb-4">
        I have a Master’s Degree in Counseling Psychology and Counselor
        Education from the University of Colorado at Denver. I am a Licensed
        Professional Counselor (LPC), Certified Hypnotherapist (CHt), and Master
        Practitioner of Rapid Resolution Therapy (MP).
      </li>
      <li class="text mb-4">
        I work with ages 12 and up. I have experience working in college
        counseling centers, a domestic violence advocacy agency, and spent
        nearly 5 years working exclusively with middle school kids and families.
        I work primarily with individual adults and adolescents.
      </li>

      <li class="text mb-4">
        I have extensive experience working with trauma, PTSD, sexual assault,
        abuse, depression, anxiety & panic, grief & loss, and sleep issues as
        well as pain management and mind-body healing.
      </li>
      <li class="text mb-4">
        I utilize Rapid Resolution Therapy (RRT) to clear your significantly
        challenging issues. After more than 12 years of working with clients who
        were struggling to come to terms with their difficult and painful
        experiences, I started seeking a better way and I ultimately found Rapid
        Resolution Therapy (RRT) which is a much faster, more effective, and
        painless way of working through challenges. Learn more about Rapid
        Resolution therapy at
        <a
          href="http://www.rapidresolutiontherapy.com"
          target="_blank"
          class="link"
        >
          www.rapidresolutiontherapy.com</a
        >
      </li>
      <li class="text mb-4">
        <img
          src="~/assets/images/jon_heather.png"
          alt="Heather and Jon"
          class="heather-jon-image bordered-image"
        />
        I train multiple times per year with Jon Connelly, PhD, LCSW creator of
        Rapid Resolution Therapy who has been developing and honing the
        methodology for more than 30 years.
      </li>
      <li class="text mb-4">
        I travel nationally to teach the Resolving Sexual Trauma course for the
        Institute of Rapid Resolution Therapy (IRRT). This is a 5 hour course
        that teaches gentle strategies for the rapid recovery of survivors of
        sexual violence and childhood abuse.
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.about-container {
  @apply mb-6;
  &::after {
    content: "";
    display: block;
    clear: both;
  }
}
.heather-jon-image {
  @apply float-right ml-2;
}
.list {
  @apply list-disc ml-8;
}
</style>
