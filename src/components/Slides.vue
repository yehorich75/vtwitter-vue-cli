<template>
    <div class="slides">
        <div class="slides-inner">
            <div v-for="slide in slides" :key="slide.i">
                <Slide :slide="slide"></Slide>
            </div>
        </div>
    </div>
</template>

<script>
import Slide from './Slide.vue';
export default {
    data () {
        return {
            slides: [
                { src: '../assets/images/slider/slider-colorful-gifts.jpg', i: 0 },
                { src: '../assets/images/slider/slider-detailed-elegance.jpg', i: 1 },
                { src: '../assets/images/slider/slider-perfect-chandeliers.jpg', i: 2 }
            ]
        }
    },
    components: {
        Slide: Slide
    }
}
</script>