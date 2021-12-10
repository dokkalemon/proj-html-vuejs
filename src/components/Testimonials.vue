<template>
<section class="testimonials full-width">

        <Title 
        title="What Our Clients Say"
        />

        <div class="slider" :class="{activeSlider: changePage}">
            <div class="slider-item">
                <div class="slider-image">
                    <img src="../assets/testimonials-2.jpg" alt="">
                </div>
                <div class="slider-text">
                    <p>Ability proceeds from a fusion of skills, knowledge, understanding and imagination, consolidated by experience.</p>
                </div>
                <div class="slider-info">
                    <h3><span>Luis Desalvo</span>, CREO TECH</h3>
                </div>
            </div>
            <div class="slider-item">
                <div class="slider-image">
                    <img src="../assets/testimonials-1.jpg" alt="">
                </div>
                <div class="slider-text">
                    <p>Ability proceeds from a fusion of skills, knowledge, understanding and imagination, consolidated by experience.</p>
                </div>
                <div class="slider-info">
                    <h3><span>Luisa Desalvo</span>, BOOL TECH</h3>
                </div>
            </div>
        </div>
        <div class="slider-nav">
            <div class="slider-nav-item" :class="{active: changePage === false}" @click="(changePage = false)"></div>
            <div class="slider-nav-item" :class="{active: changePage}" @click="(changePage = true)"></div>
        </div>

        <div class="testimonials-logos container px-15">
        <div class="line"></div>
        <div class="logos-scroll" :class="{activeLogo: changePage}">
            <div class="logo-container">
                <div class="logo">
                    <img src="../assets/clients_partner_5-200x202.png" alt="">
                </div>
                <div class="logo">
                    <img src="../assets/clients_partner_6-200x202.png" alt="">
                </div>
            </div>
            <div class="logo-container">
                <div class="logo">
                    <img src="../assets/clients_partner_1-200x202.png" alt="">
                </div>
                <div class="logo">
                    <img src="../assets/clients_partner_2-200x202.png" alt="">
                </div>
            </div>
            <div class="logo-container">
                <div class="logo">
                    <img src="../assets/clients_partner_3-200x202.png" alt="">
                </div>
                <div class="logo">
                    <img src="../assets/clients_partner_4-200x202.png" alt="">
                </div>
            </div>
        </div>
        </div>
</section>
</template>

<script>
import Title from '@/components/Title.vue'
export default {
    name: 'Testimonials',

    components: {
        Title
    },

    data() {
        return {
            changePage: false
        }
    }
}
</script>

<style scoped lang="scss">
//import var
@import '../styles/vars.scss';

.testimonials {
    background-color: #fff;
    padding-top: 100px;
    text-align: center;
    overflow: hidden;
    .slider {
        width: 200%;
        display: flex;
        position: relative;
        transition: left .4s ease;
    .slider-item {
        width: 100%;
        .slider-image {
            height: 140px;
            img {
                height: 100%;
                border-radius: 100%;
            }
        }
        .slider-text {
            padding-top: 25px;
            p {
                font-style: italic;
                width: 35%;
                margin: 0 auto;
                color: $primary-text;
                line-height: 30px;
            }
        }
        .slider-info {
            padding: 25px 0;
            h3 {
                font-size: 16px;
                font-weight: 400;
                color: $primary-title;
                span {font-weight: 700}
            }
        }
    }
    }
    .slider-nav {
        width: 100%;
        height: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        .slider-nav-item {
            height: 12px;
            width: 12px;
            margin-left: 10px;
            border-radius: 100%;
            border: 1px solid $primary-title;
            cursor: pointer;
            &:first-child {
                margin-left: 0;
            }
        }
        .active {
            background-color: $primary-title;
        }
    }
    .testimonials-logos {
        padding-top: 70px;
        overflow: hidden;
        .line {
        width: 100%;
        height: 1px;
        background-color: #bcbbbc;
        margin: 0 auto;
        
        }
        .logos-scroll {
            padding-top: 40px;
            width: 150%;
            height: 300px;
            display: flex;
            position: relative;
            .logo-container {
                width: 50%;
                height: 100%;
                display: flex;
                .logo {
                    height: 100%;
                    width: 50%;
                    cursor: pointer;
                    img {
                        height: 110px;
                    }
                }
            }
        }
    }
}

.activeLogo {
    left: -50%;
}
.activeSlider {
        left: -100%;
    }



</style>