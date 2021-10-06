<template>
  <primary-button v-bind="$attrs" v-on="$listeners">
    <span class="mr-[8px]"> Войти </span>

    <svg
      xmlns="http://www.w3.org/2000/svg"
      class="h-5 w-5 mr-[-8px]"
      fill="none"
      viewBox="0 0 24 24"
      stroke="currentColor"
    >
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="3"
        d="M9 5l7 7-7 7"
      />
    </svg>
  </primary-button>
</template>

<script>
import PrimaryButton from '@/components/Button/PrimaryButton'

export default {
  components: { PrimaryButton },
}
</script>