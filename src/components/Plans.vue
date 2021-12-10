<template>
  <section class="plans full-width">
      <div class="plans-cover">
          <img src="../assets/background1.jpg" alt="">
      </div>

        <div class="plans-container container px-15">
            <Title :secondarySet="true"
            title="Our Plans"
            />
    
        <div class="cards">
            <PlansCard v-for="(item, index) in plansArray" :key="`plans${index}`"
            :name="item.name"
            :price="item.price"
            :numberProject="item.numberProject"
            :storage="item.storage"
            :tertiarySet="item.buttonState"
            />


        </div>




        </div>
        


  </section>
</template>

<script>
import Title from '@/components/Title.vue';
import PlansCard from '@/components/PlansCard.vue';

export default {
    name: 'Plans',
    components: {
        Title,
        PlansCard,
    },
    props: {
        plansArray: Array,
    }
}
</script>

<style scoped lang="scss">
//import vars
@import '../styles/vars.scss';

.plans {
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
        padding-bottom: 80px;

        .cards {
            height: 430px;
            display: flex;
        }
    }
    
}

</style>