<template>
    <div id="sidebar">
      <div id="logo-container">
      </div>
      <live-matches></live-matches>
    </div>
</template>

<script>
import LiveMatches from '@/components/application/LiveMatches'
export default {
  name: 'Sidebar',
  components: {LiveMatches}
}
</script>

<style scoped>
  #sidebar {
    width: 300px;
    height: 100vh;
    background:#55c378;
  }

  #logo-container {
    height: 70px;
  }
</style>
