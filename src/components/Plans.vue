<template>
  <section class="plans full-width">
      <div class="plans-cover">
          <img src="../assets/background1.jpg" alt="">
      </div>

        <div class="plans-container container px-15">
            <Title :secondarySet="true"
            title="Our Plans"
            />
        </div>
        


  </section>
</template>

<script>
import Title from '@/components/Title.vue'

export default {
    name: 'Plans',
    components: {
        Title
    }
}
</script>

<style scoped lang="scss">
//import vars
@import '../styles/vars.scss';

.plans {
    height: 800px;
    position: relative;
    padding-top: 100px;
    .plans-cover {
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
    .plans-container {
        text-align: center;
        position: relative;
        z-index: 2;
    }
    
}

</style>