<template>
  <div
    class="p-[12px] flex relative items-center cursor-pointer"
    @mouseenter="onHover"
    @mouseleave="onLeave"
  >
    <span class="mr-[16px]">РУ</span>
    <svg
      xmlns="http://www.w3.org/2000/svg"
      class="h-6 w-6"
      fill="none"
      viewBox="0 0 24 24"
      stroke="currentColor"
    >
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        d="M19 9l-7 7-7-7"
      />
    </svg>

    <transition
      enter-class="opacity-0 translate-y-1.5"
      enter-active-class="transition ease-out transform"
      enter-to-class="opacity-100 translate-y-0"
      leave-class="opacity-100 translate-y-0"
      leave-active-class="transition ease-out transform"
      leave-to-class="opacity-0 translate-y-1.5"
    >
      <div
      v-show="open"
      class="
        absolute
        right-0
        top-full
        mt-full
        bg-dark-blue
        border
        border-light-blue
        border-opacity-10
        rounded-[8px]
        py-[8px]
      "
    >
      <lang-dropdown-item :active="true"> Русский </lang-dropdown-item>
      <lang-dropdown-item> English </lang-dropdown-item>
    </div>
    </transition>
  </div>
</template>

<script>
import LangDropdownItem from './LanguageDropdown/LangDropdownItem.vue'

export default {
  components: { LangDropdownItem },
  data: () => ({
    open: false,
  }),
  methods: {
    onHover() {
      this.open = true
    },
    onLeave() {
      this.open = false
    },
  },
}
</script>