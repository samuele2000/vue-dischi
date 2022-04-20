<template>
  <div id="app">
    <HeaderComp/>
    
    <main>
      <CardsSongs/>
    </main>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import CardsSongs from './components/CardsSongs.vue'

export default {
  name: 'App',
  components: {
    HeaderComp,
    CardsSongs,
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  // color: #2c3e50;
  // margin-top: 60px;
}
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
