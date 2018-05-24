<template>
    <div id="nav-filter">
      <nav-select-filter item-name="country" v-bind:item-options="countries"></nav-select-filter>
      <nav-select-filter item-name="competition" v-bind:item-options="competitions"></nav-select-filter>
      <nav-date-filter item-name="Date" v-bind:default-date="matchday"></nav-date-filter>
    </div>
</template>

<script>
import NavSelectFilter from '@/components/application/NavSelectFilter'
import NavDateFilter from '@/components/application/NavDateFilter'
export default {
  name: 'NavFilter',
  components: {NavSelectFilter, NavDateFilter},
  data: function () {
    return {
      countries: [{ id: 1, name: 'spain' }, { id: 2, name: 'france' }],
      competitions: [{ id: 1, name: 'First Division' }, { id: 2, name: 'Second Division' }],
      matchday: 'October 25th (Matchday 9)'
    }
  }
}
</script>

<style scoped>
  #nav-filter {
    display: block;
    width: 100%;
    background: #1f2532;
    height: 70px;
  }
</style>
