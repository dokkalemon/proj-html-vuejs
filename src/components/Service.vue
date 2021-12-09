<template>
  <section class="service full-width">
      <div class="service-pattern">
          <img src="../assets/pattern_background.png" alt="">
      </div>
      <div class="service-container container px-15">
          <Title :secondarySet="true"
          title="See Out Top Notch Services"
          />
      </div>
  </section>
</template>

<script>
import Title from '@/components/Title.vue'

export default {
    name: 'Service',

    components: {
        Title
    }
}
</script>

<style scoped lang="scss">
//import vars
@import '../styles/vars.scss';

.service {
    height: 850px;
    background-color: $secondary-color;
    padding-top: 120px;
    position: relative;
    .service-pattern {
        height: 100%;
        width: 100%;
        position: absolute;
        top: 0;
        img {
            height: 100%;
            width: 100%;
            object-fit: cover;
    
        }
    }
    .service-container {
    text-align: center;
}
}

</style>