<template>
  <section class="jumbo full-width">
      <div class="jumbo-cover">
          <img src="../assets/1-hero-image.png" alt="">
      </div>
      <div class="jumbo-content container">
            <div class="jumbo-text">
                <h2>SEM Campaigns Made Simple With Avada</h2>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.<br> Phasellus eu ornare erat. Curabitur pulvinar elit.</p>
                <div class="jumbo-buttons">
                    <button class="button-primary">Buy avada now</button>
                    <button class="button-secondary">Contact us</button>
                </div>
            </div>
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
    position: relative;
    .jumbo-cover {
        height: 100%;
        width: 100%;
        position: absolute;
        z-index: 1;
        top: 0;
        img {
            height: 100%;
            width: 100%;
            object-fit: cover;
        }
    }
    .jumbo-content {
        height: 100%;
        display: flex;
        align-items: center;
        position: relative;
        z-index: 2;
            .jumbo-text {
                width: 50%;
                h2 {
                    font-size: 50px;
                    font-weight: 700;
                    color: $secondary-title;
                    line-height: 60px;
                    
                }
                p {
                    color: $secondary-text;
                    margin: 25px 0;
                }
            .jumbo-buttons {
                width: 100%;
                button:first-child {
                    margin-right: 10px;
                }
            }
            
            }
    }
}




</style>