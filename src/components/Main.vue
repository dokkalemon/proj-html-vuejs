<template>
  <main>
    <Jumbo />
    

    <Section :infoTemplateArray="infoTemplateCard"/>




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

    },

    data() {
        return {
            //First Group of card
            infoTemplateCard: [
                {
                    icon: 'fas fa-road',
                    title: 'Establish Goals',
                    text: 'Aliquam non elit lacus. Praesent aliquet, ipsum id scelerisque convallis, mi ligula euismod odio, vel dictum mi risus a mi.'
                },
                {
                    icon: 'fas fa-video',
                    title: 'Work With a Team',
                    text: 'Cras semper auctor aliquam. Sed porta sed lacus sit amet consectetur. Lorem ipsum dolor sit amet, consectetur adipiscin.'
                },
                {
                    icon: 'fas fa-tint',
                    title: 'Get Results',
                    text: 'Vestibulum scelerisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus.'
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
//import Vars
@import '../styles/vars.scss';



</style>