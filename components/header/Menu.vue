<template>
  <menu class="header-menu">
    <NuxtLink
      v-for="(link, index) of links"
      :href="link.href"
      :key="index"
      class="header-menu__link"
      :class="{ 'header-menu__link_active': index === selectedLink }"
      @click="selectedLink = index"
    >
      {{ link.title }}
    </NuxtLink>
  </menu>
</template>

<script setup lang="ts">
import { Link } from "@/types/link";

const selectedLink = useCustomLink();

const links: Link[] = [
  {
    title: "Главная",
    href: "/",
  },
  {
    title: "Сервера",
    href: "/servers",
  },
  {
    title: "Скачать",
    href: "/download",
  },
  {
    title: "Открыть в браузере",
    href: "/browser",
  },
  {
    title: "Цены",
    href: "/prices",
  },
  {
    title: "Тех поддержка",
    href: "/support",
  },
  {
    title: "Контакты",
    href: "/contacts",
  },
];
</script>

<style lang="stylus">
.header-menu
  display flex
  align-items center
  justify-content space-between
  gap 2.5rem

  &__link
    color #fff
    font-weight: 300
    text-decoration none
    position relative

    &::after
      content ''
      width 100%
      position absolute
      height 1px
      background #00C5FF
      opacity 0
      transition opacity .25s
      z-index 10
      left 0
      bottom -0.25rem

    &_active
      font-weight 400

      &::after
        opacity 1
</style>
