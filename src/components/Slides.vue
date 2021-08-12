<template>
    <div class="slides">
        <div class="container">
            <div class="slides-inner">
                <div :class="slideClass" v-for="slide in slides" :key="slide.id">
                    <p>{{ singleWidth }}</p>
                    <br />
                    <p>{{ innerWidth }}</p>
                    <img :class="slideImgClass" :src="slide.src">
                    <!-- <Slide :slide="slide" /> -->
                </div>
            </div>
        </div>

    </div>
</template>

<script>
import Slide from './Slide.vue';
export default {
    // setup() {
    //     onMounted() {
    //         this.$nextTick(() => {
    //             let singleWidth = this.$el.clientWidth/this.itemsPerSlide;
    //             this.$set(this.$data, 'singleWidth', singleWidth);
    //             this.$set(this.$data, 'innerWidth', singleWidth * this.slides.length);
    //         })
    //     }
    // },
    data () {
        return {
            slides: [
                { src: require('../assets/images/slider/slider-colorful-gifts.jpg'), id: 0 },
                { src: require('../assets/images/slider/slider-detailed-elegance.jpg'), id: 1 },
                { src: require('../assets/images/slider/slider-perfect-chandeliers.jpg'), id: 2 }
            ],
            slideClass: 'slide',
            slideImgClass: 'slide__img',
            innerWidth: 0,
            singleWidth: 0
        }
    },
    props: {
        slide: ['slide'],
        itemsPerSlide: {
            type: null,
            default: 1
        }
    },
    components: {
        Slide
    },
    mounted() {
        this.$nextTick(() => {
            let singleWidth = this.$el.clientWidth/this.itemsPerSlide;
            this.$set(this.$data, 'singleWidth', singleWidth);
            this.$set(this.$data, 'innerWidth', singleWidth * this.slides.length);
        });
    }
}
</script>

<style lang="scss" scoped>

.slides {
    &-inner {
        display: flex;
        // width: 4500px;
        // overflow: hidden;
    }
}

.slide {
    width: 700px;
    img {
        max-width: 700px;
        height: auto;
    }
}

</style>style
