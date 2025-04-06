<template>
  <div class="flex flex-center">
    <EssentialLink />
    <DarkModeToggle />
  </div>
  <router-view />
</template>

<script setup>
import EssentialLink from './components/EssentialLink.vue';
import DarkModeToggle from './components/DarkModeToggle.vue';
</script>
