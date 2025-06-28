<template>
  <v-main>
    <router-view class="fade-in" />
  </v-main>

  <!-- <AppFooter /> -->
  <AppNavigationBar />
</template>

<script setup>
//
</script>

<style>
.fade-in {
  opacity: 0;
  animation: fadeIn 0.5s ease-in forwards;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
</style>
