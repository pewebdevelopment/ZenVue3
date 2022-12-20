<script setup>
import SidebarComponent from "../src/components/Sidebar/Sidebar.vue";

// import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="grid grid-cols-12">
    <SidebarComponent class="col-span-3" />
    <RouterView class="col-span-9" />
  </div>
</template>

<style scoped>
.body {
  background-color: blue;
}
</style>
