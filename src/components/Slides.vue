<template>
    <div class="slides">
        <div class="slides-inner">
            <div
                v-for="slide in slides"
                :key="slide.id"
            >
                <!-- {{slides.src}} -->
                <Slide 
                    :slide="slide"
                >
                </Slide>
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
                    { src: '../assets/images/slider/slider-colorful-gifts.jpg', id: 0 },
                    { src: '../assets/images/slider/slider-detailed-elegance.jpg', id: 1 },
                    { src: '../assets/images/slider/slider-perfect-chandeliers.jpg', id: 2 }
                ]
            }
        },
        props: {
            slide: 'slide'
        },
        components: {
            Slide: Slide
        }
    }
    
</script>