<template>
  <div class="nav-date-filter">
    <label class="label-name">{{ label.name }}</label>
    <input type="text" disabled v-bind:name="name" v-bind:value="date">
    <i class="far fa-calendar-alt"></i>
  </div>
</template>

<script>
export default {
  name: 'NavDateFilter',
  props: {
    itemName: {
      type: String,
      required: true
    },
    defaultDate: [String]
  },
  data: function () {
    return {
      name: this.itemName,
      date: this.defaultDate
    }
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
  .nav-date-filter {
    margin: 0 0 0 15px;
    padding: 15px 0;
    display: inline-block
  }

  label.label-name {
    color: #cdd1d1;
    font-size: 15px;
  }

  .nav-date-filter input {
    background: #12161f;
    color: #cdd1d1;
    padding: 0 0 0 9px;
    border-radius: 4px;
    min-width: 200px;
    margin-left: 10px;
    border: none;
    height: 30px;
    line-height: 30px;
  }

  .nav-date-filter i{
    margin-left: -25px;
    color: #55c378;
    font-size: 11px;
  }
</style>
