<template>
  <button class="block w-full px-[16px] py-[8px] hover:bg-white hover:bg-opacity-20 transition ease-out" :class="{'bg-white bg-opacity-10': active, 'bg-transparent': !active}">
      <slot></slot>
  </button>
</template>

<script>
export default {
    props: {
        active: Boolean,
    }
}
</script>