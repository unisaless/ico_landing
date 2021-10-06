<template>
  <div class="relative">
    <dynamic-component
      :is="$attrs.href ? 'a' : 'button'"
      class="
        px-[20px]
        py-[12px]
        uppercase
        font-heading font-bold
        hover:text-light-blue
        transition
        ease-out
      "
      :class="{ 'text-light-blue': active }"
    >
      <slot></slot>
    </dynamic-component>

    <transition
      enter-class="opacity-0 translate-y-1.5"
      enter-active-class="transition ease-out transform"
      enter-to-class="opacity-100 translate-y-0"
      leave-class="opacity-100 translate-y-0"
      leave-active-class="transition ease-out transform"
      leave-to-class="opacity-0 translate-y-1.5"
    >
      <div
        v-show="active"
        class="absolute top-full pointer-events-none w-full flex justify-center"
      >
        <div class="light-blob bg-light-blue w-[10px] h-[4px] rounded"></div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  props: {
    active: Boolean,
  },
}
</script>

<style scoped>
.light-blob {
  box-shadow: 0px 0px 16px #02a4fc, 0px 0px 8px #02a4fc;
}
</style>