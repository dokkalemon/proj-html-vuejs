<template>
  <div id="app">
    <Header :headerScroll="headerScroll" :headerArray="headerItem"/>

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
      headerScroll: false,

      //Header Nav Item
            headerItem: [
                {
                    label: 'Home',
                    activeState: true,
                    url: '/',
                    labelState: false
                },
                {
                    label: 'Who We Are',
                    activeState: false,
                    url: '/',
                    labelState: false
                },
                {
                    label: 'What We Do',
                    activeState: false,
                    url: '/',
                    labelState: false
                },
                {
                    label: 'Where We Eork',
                    activeState: false,
                    url: '/',
                    labelState: false
                },
                {
                    label: 'Careers',
                    activeState: false,
                    url: '/',
                    labelState: true
                },
                {
                    label: 'News',
                    activeState: false,
                    url: '/',
                    labelState: false
                },
            ],
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
