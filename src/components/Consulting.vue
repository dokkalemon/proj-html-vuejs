<template>
  <section class="consulting full-width">
      <div class="consulting-cover">
          <img src="../assets/CTA-seo-1.jpg" alt="">
      </div>

      <div class="consulting-info container px-15 ">
          <Title 
          title="Start Your Frer Consultation" 
          subtitle="Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium"
          :secondarySet="true"/>

          <div class="button">
              <button class="button-primary">contact us now</button>
          </div>
      </div>
      
  </section>
</template>

<script>
import Title from '@/components/Title.vue'

export default {
    name: 'Consulting',

    components: {
        Title
    }

}
</script>

<style scoped lang="scss">
//import vars
@import '../styles/vars.scss';

.consulting {
    height: 450px;
    position: relative;
    .consulting-cover {
        height: 100%;
        width: 100%;
        position: absolute;
        img {
            height: 100%;
            width: 100%;
            object-fit: cover;
            filter: brightness(40%);
        }
    }
    .consulting-info {
        position: relative;
        z-index: 2;
        text-align: center;
        padding-top: 100px;
    }

}



</style>