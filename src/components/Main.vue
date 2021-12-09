<template>
  <main>
    <Jumbo />
    

    <Section />




  </main>
</template>

<script>
import Jumbo from '@/components/Jumbo.vue'
import Section from '@/components/Section.vue'

export default {
    name: 'Main',
    components: {
        Jumbo,
        Section

    }
}
</script>

<style scoped lang="scss">
//import Vars
@import '../styles/vars.scss';



</style>