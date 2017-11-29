<template>
  <div id="app">
        <h1>VueSortable</h1>
          <ul v-sortable class="list-group">
            <li class="list-group-item">Maria</li>
            <li class="list-group-item">Lemmy</li>
            <li class="list-group-item">Ale</li>
          </ul>
  </div>
</template>

<script>
import Vue from 'vue'
import Sortable from 'sortablejs'

Vue.directive('sortable', {
  inserted: function (el, binding) {
    new Sortable(el, binding.value || {})
  }
})

export default {
  name: 'app',
  components: {

  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
