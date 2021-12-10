<template>
  <section class="news container px-15 debug">
    <Title title="Our News" />
  </section>
</template>

<script>
import Title from '@/components/Title.vue'

export default {
    name: 'News',
    
    components: {
      Title
    }
}
</script>

<style scoped lang="scss">
//import vars
@import '../styles/vars.scss';

.news {
  padding-top: 100px;
  text-align: center;
  height: 900px;
}


</style>