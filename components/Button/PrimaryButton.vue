<template>
  <button
    v-bind="$attrs"
    class="
      inline-flex
      items-center
      px-[24px]
      py-[12px]
      uppercase
      rounded-full
      font-bold
      text-white
      bg-light-blue
      hover:bg-opacity-80
      transition
      ease-out
    "
    v-on="$listeners"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {}
</script>
