<template>
  <main>
    <Jumbo />
    

    <Section :infoTemplateArray="infoTemplateCard"/>

    <Service :infoServiceArray="infoServiceCard"/>

    <Work :imageArray="workImage"/>

    <Plans :plansArray="plansCard"/>

    <News :postArray="post"/>

  </main>
</template>

<script>
import Jumbo from '@/components/Jumbo.vue'
import Section from '@/components/Section.vue'
import Service from '@/components/Service.vue'
import Work from '@/components/Work.vue'
import Plans from '@/components/Plans.vue'
import News from '@/components/News.vue'

export default {
    name: 'Main',
    components: {
        Jumbo,
        Section,
        Service,
        Work,
        Plans,
        News
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
            ],

            //Second Group of Card
            infoServiceCard: [
                {
                    icon: 'fab fa-google',
                    title: 'Google SEO',
                    text: 'Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.'
                },
                {
                    icon: 'fas fa-cog',
                    title: 'Brand Strategy',
                    text: 'Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.'
                },
                {
                    icon: 'fas fa-building',
                    title: 'Local SEO',
                    text: 'Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.'
                },
                {
                    icon: 'far fa-chart-bar',
                    title: 'SEO Analysis',
                    text: 'Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et, dapibus faucibus odio.'
                },
            ],

            //image for 'Our Work' Section
            workImage: [
                {
                    name: 'case-study-gallery-3-1-600x450.jpg'
                },
                {
                    name: 'case-study-gallery-2-600x450.jpg'
                },
                {
                    name: 'case-study-gallery-1-1-600x450.jpg'
                },
                {
                    name: 'case-study-gallery-4-1-600x450.jpg'
                },
                {
                    name: 'case-study-gallery-5-1-600x450.jpg'
                },
                {
                    name: 'case-study-gallery-6-1-600x450.jpg'
                },
            ],

            plansCard: [
                {
                    name: 'Standard',
                    price: '19',
                    numberProject: '5',
                    storage: '5 GB',
                    buttonState: true,
                },
                {
                    name: 'Premium',
                    price: '29',
                    numberProject: '10',
                    storage: '15 GB',
                    buttonState: true,
                },
                {
                    name: 'Professional',
                    price: '39',
                    numberProject: '15',
                    storage: '30 GB',
                    buttonState: false,
                },
                {
                    name: 'Extreme',
                    price: '59',
                    numberProject: 'Unlimited',
                    storage: 'Unlimited',
                    buttonState: true,
                }
            ],
            post: [
                {
                    thumb: 'related-service-2-320x202.jpg',
                    title: 'Why You Need A SEO Agency Now',
                    date: 'November 1st, 2017',
                    text: 'ALorem impsum dolor sit amet, consectetur adipiscing elit- in et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit.'
                },
                {
                    thumb: 'related-service-4-320x202.jpg',
                    title: 'Why You Need A SEO Agency Now',
                    date: 'November 1st, 2017',
                    text: 'ALorem impsum dolor sit amet, consectetur adipiscing elit- in et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit.'
                },
                {
                    thumb: 'blog-post-6-320x202.jpg',
                    title: 'Why You Need A SEO Agency Now',
                    date: 'November 1st, 2017',
                    text: 'ALorem impsum dolor sit amet, consectetur adipiscing elit- in et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit.'
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