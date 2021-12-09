<template>
  <section class="jumbo full-width">
      <div class="jumbo-cover">
          <img src="../assets/1-hero-image.png" alt="">
      </div>
  </section>
</template>

<script>
export default {
    name: 'Jumbo'
}
</script>

<style scoped lang="scss">
//import Vars
@import '../styles/vars.scss';

.jumbo {
    height: 800px;
    background-color: red;
    position: relative;
    .jumbo-cover {
        height: 100%;
        width: 100%;
        img {
            height: 100%;
            width: 100%;
            object-fit: cover;
        }
    }
}




</style>