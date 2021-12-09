<template>
  <section class="section full-width">
      <div class="section-content container px-15">
          <div class="section-title">
              <h2>Meet the new Agency SEO Template From The Avada Team</h2>
              <h4>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium</h4>
          </div>

          <div class="cards debug">

          </div>
      </div>
  </section>
</template>

<script>
export default {  
    name: 'Section'

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
    }
}


</style>