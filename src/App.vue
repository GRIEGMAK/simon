<template>
  <div id="app">
    <Header />
    <Main />
  </div>
</template>

<script>
import Main from './components/Main.vue'
import Header from './components/Header.vue'
import './styles/app.sass'

export default {
  name: 'App',
  components: {
    Main,
    Header
  }
}
</script>
