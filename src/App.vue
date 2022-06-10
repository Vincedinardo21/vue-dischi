<template>
  <div id="app">
    <MyHeader/>
    <ListaDischi/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import ListaDischi from './components/ListaDischi.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    ListaDischi
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
