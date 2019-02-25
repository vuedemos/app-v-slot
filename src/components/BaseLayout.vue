<template>
  <div class="container">
    <header>
      <slot name="header">我们希望把页头放在这里~</slot>
    </header>
    <main>
      <slot>我们希望把主要内容放在这里</slot>
    </main>
    <footer>
      <slot name="footer">我们希望把页脚放在这里</slot>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'BaseLayout',
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
