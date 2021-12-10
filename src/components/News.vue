<template>
  <section class="news container px-15">
    <Title 
    title="Our News" 
    subtitle="Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium"
    />

    <div class="posts"> 
      <Post v-for="(item, index) in postArray" :key="`post${index}`"
      :thumb="item.thumb"
      :title="item.title"
      :date="item.date"
      :text="item.text"
      />
      
    </div>

    <div class="button">
      <button class="button-primary">Go to news</button>
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
    },

    props: {
      postArray: Array,
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
  
  .posts {
    height: 430px;
    width: 100%;
    display: flex;
    justify-content: center;
  }
  .button {
    padding-top: 30px;
  }
}


</style>