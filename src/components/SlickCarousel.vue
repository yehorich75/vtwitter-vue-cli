<template>
    <div>
        <VueSlickCarousel :arrows="true" :dots="true">
            <div><img src="../assets/images/slider/slider-colorful-gifts.jpg" alt="Slider Image 1"></div>
            <div><img src="../assets/images/slider/slider-detailed-elegance.jpg" alt="Slider Image 2"></div>
            <div><img src="../assets/images/slider/slider-perfect-chandeliers.jpg" alt="Slider Image 3"></div>
            <div>4</div>
        </VueSlickCarousel>
    </div>
</template>

<script>
    import VueSlickCarousel from 'vue-slick-carousel'
    // optional style for arrows & dots
    import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

    export default {
        name: 'SlickCarousel',
        components: { VueSlickCarousel },
        data () {
            return {
                settings: {
                    fade: true
                }
            }
        }
    }
</script>