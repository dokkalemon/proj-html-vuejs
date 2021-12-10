<template>
  <section class="work full-width">
    <div class="work-container container px-15">
        <Title 
        title="Our Work"
        subtitle="Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium"
        />
        <div class="work-image">
            <div class="img-container" v-for="(item, index) in imageArray" :key="`img${index}`">
                <img :src="require(`../assets/${item.name}`)" alt="">
            </div>
        </div>
        <div class="work-button">
            <button class="button-primary">View our Work</button>
        </div>
    </div>
  </section>
</template>

<script>
import Title from '@/components/Title.vue'

export default {
    name: 'Work',

    components: {
        Title
    },

    props: {
        imageArray: Array,
    }
}
</script>

<style scoped lang="scss">
//import var
@import '../styles/vars.scss';

.work {
    padding-top: 100px;
    .work-container {
        text-align: center;
        .work-image {
            display: flex;
            flex-wrap: wrap;
            .img-container {
                height: 300px;
                width: calc(100% / 3);
                padding: 10px;
                img {
                    height: 100%;
                    width: 100%;
                    object-fit: cover;
                }
            }
        }
        .work-button {
            padding: 75px 0;
        }
    }
}

</style>