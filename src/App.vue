<script setup>
import theHeader from './components/navigation/the-header.vue'
import appAsideList from './components/app-asideList.vue'
import appCrash from './components/app-crash.vue'
import appMenu from './components/app-menu.vue'
import theFooter from './components/navigation/the-footer.vue'
</script>

<template>
  <div class="container">
    <the-header />
    <div class="wrapper">
      <app-crash />
      <app-menu />
      <app-aside-list />
    </div>
  </div>
  <the-footer />
</template>

<style scoped>

</style>
