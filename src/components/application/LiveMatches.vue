<template>
  <div class="live-matches">
    <h2 class="sidebar-heading">On live matches <span><i class="far fa-arrow-alt-circle-right"></i></span></h2>
    <ul>
      <li class="active">2 - 0 <span><i class="far fa-circle"></i> Chelsea - Man United</span></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'LiveMatches'
}
</script>

<style scoped>
  .live-matches {
    display: block;
    background: #1f2532;
  }

  .live-matches ul {
    width: 100%;
    padding: 0;
    margin: 0;
  }

  .live-matches ul li {
    width: 100%;
    list-style: none;
    padding: 10px;
    box-sizing: border-box;
  }

  .live-matches ul li span{
    font-size: 14px;
    margin-left: 5px;
  }

  .live-matches ul li.active {
    color: #222631;
    background: #f4f5f6;
    border-left: 3px solid #55c378;
  }
</style>
