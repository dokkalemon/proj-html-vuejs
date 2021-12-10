<template>
  <section class="news container px-15 debug">
    <Title title="Our News" />

    <div class="posts">
      <Post />
    </div>
  </section>
</template>

<script>
import Title from '@/components/Title.vue'
import Post from '@/components/Post.vue'

export default {
    name: 'News',
    
    components: {
      Title,
      Post
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