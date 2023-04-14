<template>
  <NuxtLayout name="default">
    <div class="">some text</div>
  </NuxtLayout>
</template>

<script setup lang="ts">
const currentLink = useCustomLink();

watch(currentLink, (value) => {
  console.log(value);
});
</script>
