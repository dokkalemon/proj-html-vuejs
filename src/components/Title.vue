<template>
    <div class="section-title">
        <h2>{{title}}</h2>
        <h4>{{subtitle}}</h4>
    </div>
</template>

<script>
export default {
    name: 'Title',

    props: {
        title: String,
        subtitle: String,
    }
}
</script>

<style scoped lang="scss">
//import vars
@import '../styles/vars.scss';

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

</style>