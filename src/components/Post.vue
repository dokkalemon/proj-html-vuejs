<template>
    <section class="post ">
        <div class="post-container">
            <div class="post-image">
                <img :src="require(`../assets/${thumb}`)" alt="">
            </div>

            <div class="post-title">
                <h3>{{title}}</h3>
            </div>

            <div class="post-date">
                <p>{{date}}</p>
            </div>

            <div class="post-text">
                <p>{{text}}</p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Post',

    props: {
        title: String,
        date: String,
        text: String,
        thumb: String
    }
}
</script>

<style scoped lang="scss">
//import vars
@import '../styles/vars.scss';

.post {
    height: 100%;
    width: 100%;
    padding: 0px 10px 0px 10px;
    .post-container {
        height: 100%;
        width: 100%;
        .post-image {
            width: 100%;
            img {
                width: 100%;
            }
        }
        .post-title {
            padding-top: 10px;
            h3 {
                color: $tertiary-title;
                font-size: 20px;
            }
        }

        .post-date {
            padding-top: 5px;
            p {
                font-size: 11px;
                color: $primary-text;
            }
        }
        .post-text {
            padding-top: 10px;
            p {
                color: $primary-text;
                width: 95%;
                margin: 0 auto;
                font-size: 14px;
                line-height: 30px;
            }

        }
    }
    &:first-child {
        padding: 0px 10px 0px 0px
    }
    &:last-child {
        padding: 0px 0px 0px 10px
    }
}


</style>