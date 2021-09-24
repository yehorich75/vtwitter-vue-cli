<template>
    <carousel :items-to-show="1">     
            <img :class="slideImgClass" :src="src">
            <div class="top__slider-info">
                <h2 class="top__slider-title">{{ title }}</h2>
                <p class="top__slider-text">{{ text }}</p>
            </div>

        <template #addons>
            <navigation />
            <pagination />
        </template>
    </carousel>
</template>

<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';
// import SlideItem from '../components/SlideItem';

export default {
    name: 'Slides',
    components: {
        Carousel,
        Slide,
        Pagination,
        Navigation,
        // SlideItem
    },
    props: {
        id: Number, 
        src: String, 
        alt: String, 
        title: String, 
        text: String
    }

};
</script>

<style lang="scss" scoped>

.carousel {
    &__slide {
        align-items: start;
        img {
            max-width: 700px;
            height: auto;
        }
    }
}


</style>