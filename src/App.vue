<template>
  <div id="app">
    <Header />

    <Main />


  </div>
</template>

<script>
//FontAwesome Package
import '@fortawesome/fontawesome-free/css/all.css'

//Components
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main
    
  }
}
</script>

<style lang="scss">
@import './styles/global.scss';




</style>
