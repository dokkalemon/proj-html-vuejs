<template>
  <div id="app">
    <Header :headerScroll="headerScroll"/>

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
    Main,
  },

  data() {
    return {
      headerScroll: false
    }
  },

  created () {
    window.addEventListener('scroll', this.scrollPage);
  },
  destroyed () {
    window.removeEventListener('scroll', this.scrollPage);
  },
  methods: {

    //Function for Header Background on scroll page
    scrollPage () {
      this.headerScroll = true;
    }
  }
  
}
</script>

<style lang="scss">
@import './styles/global.scss';




</style>
