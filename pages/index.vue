<template>
  <wrapper>
    <top-header></top-header>
    <div class="w-[1110px] mx-auto">
      <hero></hero>
      <div class="my-[12px]"></div>
      <countdown></countdown>
      <div class="my-[24px] h-56"></div>
      <about-section></about-section>
    </div>
    <div style="height: 2000px"></div>
  </wrapper>
</template>

<script>
import Countdown from '~/components/Countdown.vue'
import Hero from '~/components/Hero.vue'
import AboutSection from '~/components/AboutSection.vue'
export default {
  components: { Hero, Countdown, AboutSection },
}
</script>
