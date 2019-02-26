<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <SlotDemo />

    <SlotDemo v-slot:default>
      <p>v-slot:default 的使用</p>
    </SlotDemo>

    <SlotDemo>
      <template v-slot:default>
        <h3>v-slot:default</h3>
      </template>
    </SlotDemo>

    <BaseLayout>
      <h1 slot="header">Vue 2.6之前具名插槽</h1>
      <p>我是页面的主内容</p>
      <p slot="footer">&copy;w3cplus</p>
    </BaseLayout>

    <BaseLayout>
      <template v-slot:header>
        <h1>Vue 2.6之后具名插槽</h1>
      </template>
      <template v-slot:default>
        <p>我是页面的主内容</p>
      </template>
      <template v-slot:footer>
        <p>&copy;w3cplus</p>
      </template>
    </BaseLayout>

    <BaseLayout>
      <template #header>
        <h1>Vue 2.6之后具名插槽</h1>
      </template>
      <template #default>
        <p>我是页面的主内容</p>
      </template>
      <template #footer>
        <p>&copy;w3cplus</p>
      </template>
    </BaseLayout>
    <h2>Vue 2.6 版本前</h2>
    <List :items="colors">
      <template slot-scope="color" slot="default">
        <div :style="{backgroundColor: color.hex}"> {{ color.name }}</div>
      </template>
    </List>

     <h2>Vue 2.6 版本后</h2>
    <List :items="colors" v-slot="color">
      <div :style="{backgroundColor: color.hex}"> {{ color.name }}</div>
    </List>
  </div>
</template>

<script>
import SlotDemo from './components/SlotDemo'
import BaseLayout from './components/BaseLayout'
import List from './components/List'

export default {
  name: 'app',
  components: {
    SlotDemo,
    BaseLayout,
    List
  },
  data () {
    return {
      colors: [
        { name: 'Yellow', hex: '#F4D03F', },
        { name: 'Green', hex: '#229954' },
        { name: 'Purple', hex: '#9B59B6' }
      ]
    }
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
