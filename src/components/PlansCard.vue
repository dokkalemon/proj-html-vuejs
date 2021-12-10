<template>
    <section class="plans-card">
        <div class="plans-card-container">
            <div class="plans-title">
                <h2>{{name}}</h2>
            </div>

            <div class="plans-price">
                <span>&#36;</span>
                <h3>{{price}}</h3>
                <div class="plans-price-item">
                    <h5>99</h5>
                    <span>monthly</span>
                </div>
            </div>
            <div class="plans-details">
                <p>{{numberProject}} Project</p>
                <p>{{storage}} Storage</p>
                <p>Unlimited Users</p>
            </div>
            <div class="plans-button">
                <button class="button-primary" :class="{buttonTertiary: tertiarySet}">START TODAY</button>
            </div>




        </div>
    </section>
</template>

<script>
export default {
    name: 'PlansCard',

    props: {
        name: String,
        price: String,
        numberProject: String,
        storage: String,
        tertiarySet: Boolean,
    }
}
</script>

<style scoped lang="scss">
//Import vars
@import '../styles/vars.scss';

.plans-card {
    height: 100%;
    width: 100%;
    padding: 5px;
    .plans-card-container {
        height: 100%;
        width: 100%;
        background-color: #fff;
        .plans-title {
            padding-top: 30px;
            h2 {
                color: $primary-title;
                letter-spacing: -1px;
                font-size: 22px;
            }
        }
        .plans-price {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 20px;
            span {
                color: #5d5c5d;
                font-weight: 800;
                font-size: 18px;
                margin-top: -10px;
            }
            h3 {
                color: $price-color;
                font-size: 40px;
            }
            .plans-price-item {
                margin-left: 2px;
                display: flex;
                flex-direction: column;
                align-items: flex-start;
                justify-content: center;
                h5 {
                    color: $price-color;

                }
                span {
                    font-size: 10px;
                    font-weight: 500;
                    font-style: italic;
                    margin-top: 0
                }
            }
            
        }
        .plans-details {
            p {
                color: $primary-text;
                padding-top: 35px;
            }
        }
        .plans-button {
            padding-top: 35px;
        }
    }
    &:first-child {
        padding: 5px 5px 5px 0px
    }
    &:last-child {
        padding: 5px 0px 5px 5px
    }
}



</style>