<template>
  <top-nav 
    class="ccm-main-menu" 
    project-logo="Claudio Mendonca Design" 
    :menu-data="menu"
    color-mode="positive"
  />
</template>

<script setup>
import { menu } from '~/composables/navigation.js'
</script>

<style lang="scss" scoped>
:deep(a) {
  color: var(--base-color);
  font-family: var(--body-font);
  font-weight: 200;
}

:deep(.top-nav__menu-link) {
  color: var(--base-color);
  font-family: var(--body-font);
  font-weight: 200;
}

:deep(a:hover) {
  text-decoration: none;
  cursor: pointer;
}

</style>
