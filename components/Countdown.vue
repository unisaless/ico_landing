<template>
  <div class="relative z-10">
    <div class="flex items-center justify-between mb-[24px]">
      <div class="text-light-blue font-bold uppercase">
        Pre-sale закончиться через
      </div>
      <div class="text-light-blue font-bold uppercase">10$ = 1GRC</div>
    </div>
    <div class="timer p-[24px] flex rounded-[16px] select-none">

        <div class="w-1/4 border-r border-white border-opacity-10 flex flex-col items-center justify-center py-[24px]">
            <div class="text-[72px] font-heading leading-none mb-[12px]">
                {{ parseInt((this.to - this.current) / 1000 / 60 / 60 / 24) }}
            </div>
            <div class="font-heading uppercase text-light-blue font-bold">
                Дней
            </div>
        </div>
        <div class="w-1/4 border-r border-white border-opacity-10 flex flex-col items-center justify-center py-[24px]">
            <div class="text-[72px] font-heading leading-none mb-[12px]">
                {{ parseInt((this.to - this.current) / 1000 / 60 / 60 % 24) }}
            </div>
            <div class="font-heading uppercase text-light-blue font-bold">
                Часов
            </div>
        </div>
        <div class="w-1/4 border-r border-white border-opacity-10 flex flex-col items-center justify-center py-[24px]">
            <div class="text-[72px] font-heading leading-none mb-[12px]">
                {{ parseInt((this.to - this.current) / 1000 / 60 % 60) }}
            </div>
            <div class="font-heading uppercase text-light-blue font-bold">
                Минут
            </div>
        </div>
        <div class="w-1/4 flex flex-col items-center justify-center py-[24px]">
            <div class="text-[72px] font-heading leading-none mb-[12px]">
                {{ parseInt((this.to - this.current) / 1000 % 60) }}
            </div>
            <div class="font-heading uppercase text-light-blue font-bold">
                Секунд
            </div>
        </div>

    </div>
  </div>
</template>

<script>
export default {
    mounted() {
        this.to = Date.parse('10.08.2021');
        this.current = Date.now();

        setInterval(() => {
            this.current = Date.now()
        }, 1000);
    },
    data: () => ({
        to: null,
        current: null,
    }),
    computed: {
    }
}
</script>

<style>
.timer {
  background: linear-gradient(
    90deg,
    rgba(126, 229, 255, 0.1) 3.12%,
    rgba(65, 169, 255, 0.1) 100%
  );
}
</style>