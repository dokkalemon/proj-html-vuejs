<template>
  <section class="section full-width">
      <div class="section-content container px-15">
          <div class="section-title">
              <h2>Meet the new Agency SEO Template From The Avada Team</h2>
              <h4>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium</h4>
          </div>

          <div class="section-cards">
              <PrimaryCard :primarySet="true" 
              icon="fas fa-road"
              text="Aliquam non elit lacus. Praesent aliquet, ipsum id scelerisque convallis, mi ligula euismod odio, vel dictum mi risus a mi."
              title="Establish Goals"
              />
              <PrimaryCard :primarySet="true"
              icon="fas fa-video"
              title="Work With a Team"
              text="Cras semper auctor aliquam. Sed porta sed lacus sit amet consectetur. Lorem ipsum dolor sit amet, consectetur adipiscin."
              />
              <PrimaryCard :primarySet="true"
              icon="fas fa-tint"
              title="Get Results"
              text="Vestibulum scelerisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus."
              />
          </div>

          <div class="section-image">
              <img src="../assets/agency-seo-desk-front-1200x570.jpg" alt="">
          </div>
      </div>
  </section>
</template>

<script>
import PrimaryCard from '@/components/PrimaryCard.vue'

export default {  
    name: 'Section',
    components: {
        PrimaryCard,
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
        .section-title {
            padding-bottom: 80px;
            h2 {
            width: 50%;
            font-size: 30px;
            margin: 0 auto;
            color: $primary-title;
            padding-bottom: 20px;
            }
            h4 {
                color: $primary-text;
                font-weight: 500;
                width: 45%;
                margin: 0 auto;
            }
        }
        .section-cards {
            display: flex;
        }
        .section-image {
            margin-top: 20px;
        }
    }
}


</style>