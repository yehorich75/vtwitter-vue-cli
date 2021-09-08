<template>
    <carousel :items-to-show="1">
        <slide v-for="slide in slides" :key="slide.id">
            <!-- {{ slide.src }} -->
            <img :class="slideImgClass" :src="slide.src">
            <div class="top__slider-info">
                <h2 class="top__slider-title">{{ slide.title }}</h2>
                <p class="top__slider-text">{{ slide.text }}</p>
            </div>
        </slide>

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
    data (){
        return {
            slides: [
                {
                    id: '1',
                    src: require('../assets/images/slider/slider-colorful-gifts.jpg'), 
                    alt: 'Slider Image 1',
                    title: 'Чудові подарунки',
                    text: 'Deep v you probably havent heard of them banh mi synth actually affogatAesthetic lyft ethical drinking vinegar austint'},
                {
                    id: '2',
                    src: require('../assets/images/slider/slider-detailed-elegance.jpg'),
                    alt: 'Slider Image 2',
                    title: 'Детальна елегантність', 
                    ext: 'Deep v you probably havent heard of them banh mi synth actually affogatAesthetic lyft ethical drinking vinegar austint'},
                {
                    id: '3',
                    src: require('../assets/images/slider/slider-perfect-chandeliers.jpg'),
                    alt: 'Slider Image 3',
                    title: 'Ідеальні люстри',
                    text: 'Deep v you probably havent heard of them banh mi synth actually affogatAesthetic lyft ethical drinking vinegar austint'}
            ],
            slideClass: 'slide',
            slideImgClass: 'slide__img'
        }
    }
};
</script>

<style lang="scss" scoped>

.carousel {
    &__slide {
        img {
            max-width: 700px;
            height: auto;
        }
    }
}


</style>