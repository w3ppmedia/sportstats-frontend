<template>
  <div class="nav-select-filter">
    <label class="label-name">{{ label.name }}</label>
    <select>
      <option v-for="option in options" :key="option.id" :value="option.id">{{ capitalize(option.name) }}</option>
    </select>
    <i class="fas fa-sort-down"></i>
  </div>
</template>

<script>
export default {
  name: 'NavSelectFilter',
  props: {
    itemName: {
      type: String,
      required: true
    },
    itemOptions: [Array]
  },
  data: function () {
    return { options: this.itemOptions }
  },
  computed: {
    label: function () {
      return {
        name: this.capitalize(this.itemName)
      }
    }
  }
}
</script>

<style scoped>
  .nav-select-filter {
    margin: 0 0 0 15px;
    padding: 20px 0;
    display: inline-block;
  }
  label.label-name {
    color: #cdd1d1;
    font-size: 15px;
  }
  .nav-select-filter select {
    background: #12161f;
    color: #cdd1d1;
    padding: 5px 9px;
    border-radius: 1px;
    height: 30px;
    min-width: 180px;
    vertical-align: middle;
    margin-left: 10px;
    border: none;
    -moz-appearance:none; /* Firefox */
    -webkit-appearance:none; /* Safari and Chrome */
    appearance:none;
  }
  .nav-select-filter i{
    margin-left: -23px;
    color: #55c378;
    font-size: 13px;
  }
</style>
