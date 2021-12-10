<template>
  <header class="full-width" :class="{active: headerScroll}">
      <div class="header container px-15">
          <div class="header-logo">
              <img src="../assets/logo_seo_w_1x.png" alt="">
          </div>
          <nav class="header-link">
              <ul>
                  <li v-for="(item, index) in headerArray" :key="`headerItem${index}`"><a href="" :class="{active: item.activeState, label: item.labelState}" >{{item.label}}</a></li>
              </ul>
          </nav>
          <div class="header-button">
              <button class="button-primary">Get in touch now</button>
          </div>
      </div>
  </header>
</template>

<script>
export default {
    name: 'Header',

    props: {
        headerScroll: Boolean,
        headerArray: Array
    }
}
</script>

<style scoped lang="scss">
//import vars;
@import '../styles/vars.scss';

header {position: fixed; z-index: 999; transition: all 0.4s ease}
header.active {
    background-color: #051745;
    .header {
        height: 60px;
        transition: all 0.4s ease
    }   
}
.header {
    height: 100px;
    display: flex;
    .header-logo {
        height: 100%;
        display: flex;
        align-items: center;
        img {
            height: 40px;
        }
    }
    .header-link {
        flex-grow: 1;
        height: 100%;
        padding: 0px 30px;
        ul {
            height: 100%;
            width: 100%;
            display: flex;
            list-style: none;
            justify-content: flex-end;
            align-items: center;
            li {
                margin-left: 30px;
                font-size: 14px;
                text-transform: capitalize;
                a {
                    color: $secondary-text;
                    &:hover {
                        color: $link-color-active;
                    }
                }
                .active {
                    color: $link-color-active;
                }

                .label:after {
                    content: 'Apply';
                    border: 1px solid $primary-color;
                    border-radius: 5px;
                    color: $primary-color;
                    text-transform: uppercase;
                    font-size: 10px;
                    padding: 2px 4px;
                    margin-left: 5px;
                }
            }
        }
    }
    .header-button {
        display: flex;
        align-items: center;
    }
}

</style>