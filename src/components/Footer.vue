<template>
  <footer class="full-width">
      <div class="footer container px-15 debug">
          <div class="footer-logo">
              <img src="../assets/logo_seo_1x.png" alt="">
          </div>

          <div class="footer-nav">
              <ul>
                  <li><a href="" class="active">Home</a></li>
                  <li><a href="">Home</a></li>
                  <li><a href="">Home</a></li>
                  <li><a href="">Home</a></li>
                  <li><a href="">Home</a></li>
                  <li><a href="">Home</a></li>
                  <li><a href="">Home</a></li>
              </ul>
          </div>




      </div>
      


  </footer>




</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style scoped lang="scss">
//import vars
@import '../styles/vars.scss';

footer {
    height: 350px;
    .footer {
        padding-top: 50px;
        .footer-logo {
            text-align: center;
        }
        .footer-nav {
            width: 100%;
            display: flex;
            padding: 50px 0; 
            ul {
                width: 100%;
                list-style: none;
                display: flex;
                justify-content: center;
                li {
                    margin-right: 40px;
                    a {
                        font-size: 12px;
                        color: $primary-text;
                        &:hover {
                            color: $primary-color;
                        }
                    }
                    .active {color: $primary-color}
                }
            }

        }
    }
}

</style>