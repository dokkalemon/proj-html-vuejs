<template>
  <section class="card" >
    <div class="card-container " :class="{primary: primarySet, secondary: secondarySet}">
        <div class="card-icon">
            <i :class="icon"></i>
        </div>
        <div class="card-title">
            <h3>{{title}}</h3>
        </div>
        <div class="card-text">
            <p>{{text}}</p>
        <div class="card-more" v-show="secondarySet">
            <a href="">Read More ></a>
        </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    name: 'PrimaryCard',
    props: {
        primarySet : Boolean,
        secondarySet : Boolean,
        icon: String,
        title: String,
        text: String
    }
}
</script>

<style scoped lang="scss">
//import vars
@import '../styles/vars.scss';
.card {
    width: 100%;
    height: 100%;
    padding: 10px;
    &:first-child {
        padding: 0;
        padding: 10px 10px 10px 0px;
    }
    &:last-child {
        padding: 0;
        padding: 10px 0px 10px 10px;
    }
    
    .card-container {
        height: 100%;
        width: 100%;
        .card-icon {
            height: 100px;
            display: flex;
            justify-content: center;
            align-items: center;
            i {
                color: $primary-color;
                font-size: 30px;
            }
        }
        .card-title {
            font-size: 20px;
            color: $primary-title;
        }
        .card-text {
            padding: 15px 40px 35px 40px;
            color: $primary-text;
            font-size: 14px;
            line-height: 25px;
            font-weight: 500;
            text-align: center;
        }

        .card-more {
            padding-top: 15px;
            a {
                color: $primary-color;

                &:hover {
                    opacity: 0.5

                }
            }
        }
    }
    .primary {
        background-color: #fff;
    }

    .secondary {
        background-color: $tertiary-color;
        .card-title {
            color: white;
        }
        .card-text {
            color: $secondary-text;
        }
        
    }
}

</style>