<template>
  <div id="app">
    <div class="wrapper">
      <sidebar></sidebar>
      <nav-filter></nav-filter>
      <router-view/>
    </div>
  </div>
</template>
<script>
import NavFilter from '@/components/application/NavFilter'
import Sidebar from '@/components/application/Sidebar'
export default {
  name: 'App',
  components: {Sidebar, NavFilter}
}
</script>
<style src="./assets/css/fontawesome-all.min.css"></style>
<style src="./assets/css/main.css" ></style>
<style src="./assets/css/font.css" ></style>
<style src="./assets/css/app.css" ></style>
