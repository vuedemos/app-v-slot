<template>
  <div class="color-list">
    <h2>{{ title }}</h2>
    <div class="list">
      <div class="list-item" v-for="(item, index) in items" :key="index">
        <slot v-bind="item"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ColorList',
  props: {
    title: {
      type: String,
      default: 'Colors'
    },
    items: {
      type: Array
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
