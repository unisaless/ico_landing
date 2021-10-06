<template>
  <section class="flex items-center">
      <div class="flex-1 py-24 relative z-10">

        <h1 class="text-[48px] font-bold font-heading leading-[58px] mb-[24px]">
            Цифровая <br> 
            революция Вашего <br>
            бизнеса
        </h1>

        <p class="font-heading text-white text-opacity-95 font-bold uppercase mb-[32px]">
            Универсальное решение для бизнес индустрии <br> на основе цифровых технологий
        </p>

        <primary-button>
            Купить токены
        </primary-button>

      </div>

      <div class="flex items-center justify-center relative">
          <img src="/images/hero_gradient.png" class="absolute min-w-[1500px] z-0" alt="">
          <img class="max-w-[450px] realtive z-10" src="/images/hero_proccess.png" />
      </div>
  </section>
</template>

<script>
import PrimaryButton from './Button/PrimaryButton.vue'
export default {
  components: { PrimaryButton },

}
</script>
