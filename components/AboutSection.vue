<template>
  <section class="flex items-center relative z-10">
    <div class="w-2/5 flex items-center justify-center relative z-10">
        <img src="/images/about_gradient.png" class="absolute min-w-[1000px] z-0" alt="gradient">
      <img src="/images/about_logo.png" class="max-w-[420px] relative z-10" alt="logo" />
    </div>

    <div class="w-3/5 pl-[56px]">
        <div class="font-bold text-light-blue uppercase font-heading mb-[8px]">
            О компании
        </div>
        <img src="/images/about_universal.png" class="h-[50px]" alt="">
        <div class="text-[59px] font-heading font-bold mb-[24px]">
            Sales Software
        </div>

        <p class="text-[24px] mb-[24px]">
            Динамически развивающаяся IT компания с успешным бэкграундом, производим digital - продукты и сервисы для бизнеса, создаём решения нового поколения. 
        </p>
        <p class="text-[24px] mb-[36px]">
            Наши клиенты всегда впереди своих конкурентов!
        </p>

        <primary-button>
            Whitepaper
        </primary-button>
    </div>
  </section>
</template>

<script>
import PrimaryButton from './Button/PrimaryButton.vue'
export default {
    components: {PrimaryButton},
}
</script>

PrimaryButton