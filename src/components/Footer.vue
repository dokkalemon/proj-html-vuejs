<template>
  <footer class="full-width">
      <div class="footer container px-15">
          <div class="footer-logo">
              <img src="../assets/logo_seo_1x.png" alt="">
          </div>

          <div class="footer-nav">
              <ul>
                  <li v-for="(item, index) in footerArray" :key="`footer${index}`"><a :href="item.url" :class="{active: item.activeState}">{{item.label}}</a></li>
              </ul>
          </div>

          <div class="copyright">
              <p>© Copyright 2012 -2020 | Avada Theme by <a href="">ThemeFusion</a> | All Rights Reserved | Powered by <a href="">WordPress</a></p>
          </div>

          <div class="footer-socials">
              <i class="fab fa-facebook-f"></i>
              <i class="fab fa-instagram"></i>
              <i class="fab fa-twitter"></i>
              <i class="fab fa-youtube"></i>

          </div>




      </div>
      <a href="#top">
          <div class="arrow-up">
                <i class="fas fa-chevron-up"></i>
            </div>
        </a>

  </footer>




</template>

<script>
export default {
    name: 'Footer',

    props: {
        footerArray: Array,
    }
}
</script>

<style scoped lang="scss">
//import vars
@import '../styles/vars.scss';

footer {
    height: 350px;
    position: relative;
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
                    &:last-child {
                        margin-right: 0;
                    }
                }
            }

        }
        .copyright {
            width: 100%;
            text-align: center;
            p {
                font-size: 12px;
                color: #8a8a8a;
                a {
                    color: $primary-title
                }
            }
        }

        .footer-socials {
            width: 100%;
            display: flex;
            justify-content: center;
            padding-top: 40px;
            i {
                color: $primary-text;
                margin-right: 20px;
                font-size: 22px;
                cursor: pointer;
                transition: all .4s ease;
                &:hover {
                    color: $primary-color;
                }
                &:last-child {
                    margin-right: 0;
                }
            }
        }
    }
    a {
        .arrow-up {
        height: 30px;
        width: 37px;
        background-color: $primary-text;
        position: absolute; 
        right: 10%;
        bottom: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 5px 5px 0px 0;
        cursor: pointer;
        transition: all .4s ease;
        i {
            color: white;
        }
        }
        &:hover .arrow-up {
            background-color: $primary-title
        }
    }
}

</style>