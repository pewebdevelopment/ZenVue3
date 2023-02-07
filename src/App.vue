<script setup>
import SidebarComponent from "../src/components/Sidebar/Sidebar.vue";

import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="grid grid-cols-12">
    <SidebarComponent class="col-span-3" />
    <RouterView class="col-span-9" />
  </div>
</template>

<style scoped>
.body {
  background-color: green;
  position:relative;
}
.grid-cols-12{
  display:flex;
}
.col-span-9{
  position:fixed;
  left:45%;
  top:2rem;
  height:90vh;
  width:55%;
  background-color:grey;
  text-align:center;
  padding-top:2rem;
  font-size:25px;
  overflow-y: scroll;
  border-radius:20px;


 
}
</style>
