<template>
  <section class="section full-width">
      <div class="section-content container px-15">
        
          <Title
          title="Meet the new Agency SEO Template From The Avada Team"
          />
          <div class="section-cards">
              <PrimaryCard :primarySet="true" v-for="(item, index) in infoTemplateArray" :key="`key${index}`"
              :icon="item.icon"
              :title="item.title"
              :text="item.text"
              />
          </div>
          <div class="section-image">
              <img src="../assets/agency-seo-desk-front-1200x570.jpg" alt="">
          </div>
      </div>
  </section>
</template>

<script>
import Title from '@/components/Title.vue'
import PrimaryCard from '@/components/PrimaryCard.vue'

export default {  
    name: 'Section',
    components: {
        PrimaryCard,
        Title
    },

    props: {
        infoTemplateArray: Array,
    }

}
</script>

<style scoped lang="scss">
//import Vars
@import '../styles/vars.scss';

.section {
    .section-content {
        padding-top: 100px;
            text-align: center;
        .section-cards {
            display: flex;
        }
        .section-image {
            height: 100%;
            width: 100%;
            margin-top: 20px;
            display: flex;
        }
    }
}


</style>