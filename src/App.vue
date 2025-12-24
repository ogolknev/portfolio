<script setup lang="ts">
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import MainPage from './pages/MainPage.vue';

</script>

<template>
  <div class="w-dvw h-dvh overflow-scroll">
    <AppHeader />
    <main class="w-8/10 max-w-250 bg-neutral-900 mx-auto">
      <MainPage />
    </main>
    <AppFooter />
  </div>
</template>