<template>
  <header class="header">
    <NuxtLink href="/">
      <img src="@/assets/icons/logo.svg" alt="logo" class="header__logo" />
    </NuxtLink>
    <HeaderMenu />
  </header>
</template>

<script setup lang="ts"></script>

<style lang="stylus">
.header
  padding 2.75rem 7rem
  background #141C24
  display flex
  align-items center
  gap 6.5rem

  &__logo
    cursor pointer
    width 11.875rem
    height 1.75rem
</style>
