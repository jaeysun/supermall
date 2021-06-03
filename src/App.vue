<template>
  <router-view/>
  <main-tab-bar></main-tab-bar>
</template>

<script>

import MainTabBar from './components/content/mainTabbar/MainTabBar.vue';

export default {
    components: {
      MainTabBar
    }
}
</script>

<style>

</style>
