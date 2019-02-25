<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <SlotDemo>
      <div class="box">
        <h1>Slot Demo</h1>
        <p>This is slot demo!</p>
      </div>
    </SlotDemo> -->

    <!-- <div class="box">
      <SubmitButton />
      <SubmitButton>保存</SubmitButton>
    </div> -->

    <!-- <BaseLayout>
      <h1 slot="header">我是一个页头</h1>
      <p slot="footer">&copy;w3cplus</p>
    </BaseLayout> -->

    <ColorList :items="colors" title="Colors">
      <template scope="color">
        <div :style="{background: color.hex}">{{ color.name }}</div>
      </template>
    </ColorList>
  </div>
</template>

<script>
// import SlotDemo from './components/SlotDemo'
// import SubmitButton from './components/SubmitButton'
// import BaseLayout from './components/BaseLayout'
import ColorList from './components/ColorList'

export default {
  name: 'app',
  components: {
    // SlotDemo,
    // SubmitButton
    // BaseLayout
    ColorList
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
