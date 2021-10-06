<template>
  <div>
    <div class="h-[80px]"></div>
    <div
      class="
        h-[80px]
        bg-[#0D053A]
        p-[24px]
        flex
        items-center
        bg-opacity-80
        fixed
        w-full
        top-0
        z-40
        backdrop-filter
        backdrop-blur-lg
      "
    >
      <header-logo />
      <header-divider />

      <div class="ml-auto flex items-center h-full">
        <div class="flex ml-[12px]">
          <header-link :active="true"> Главная </header-link>
          <header-link> О компании </header-link>
          <header-link> О проекте </header-link>
          <header-link> Дорожная карта </header-link>
          <header-link> GRC Токены </header-link>
        </div>

        <header-divider />

        <div class="mx-[12px]">
          <language-dropdown />
        </div>

        <login-button />
      </div>
    </div>
  </div>
</template>

<script>
import HeaderDivider from './TopHeader/HeaderDivider.vue'
import HeaderLogo from './TopHeader/HeaderLogo.vue'
import LanguageDropdown from './TopHeader/LanguageDropdown.vue'
import LoginButton from './TopHeader/LoginButton.vue'
import HeaderLink from './TopHeader/HeaderLink.vue'
export default {
  components: {
    HeaderLogo,
    HeaderDivider,
    LanguageDropdown,
    LoginButton,
    HeaderLink,
  },
}
</script>,
    LoginButton