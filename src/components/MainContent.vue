<template>
    <main class="main-content">
        <div class="top">
            <div class="top__inner">
                <div class="container">
                    <Slides />
                    <SlickCarousel v-bind="settings" />
                </div>
            </div>
        </div>    
    </main>
</template>

<script>

    import Slides from '@/components/Slides.vue';
    import VueSlickCarousel from 'vue-slick-carousel'
    // optional style for arrows & dots
    import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

    export default ({
        name: 'MainContent',
        components: {
            Slides,
            VueSlickCarousel
        },
        data (){
            return {
                sliderItems: [
                    {
                        id: '1',
                        image: 'slider-colorful-gifts.jpg', 
                        alt: 'Slider Image 1',
                        title: 'Чудові подарунки',
                        text: 'Deep v you probably havent heard of them banh mi synth actually affogatAesthetic lyft ethical drinking vinegar austint'},
                    {
                        id: '2',
                        image: 'slider-detailed-elegance.jpg',
                        alt: 'Slider Image 2',
                        title: 'Детальна елегантність', 
                        text: 'Deep v you probably havent heard of them banh mi synth actually affogatAesthetic lyft ethical drinking vinegar austint'},
                    {
                        id: '3',
                        image: 'slider-perfect-chandeliers.jpg',
                        alt: 'Slider Image 3',
                        title: 'Ідеальні люстри',
                        text: 'Ефектні шедеври освітлення, зроблені з кращих матеріалів Землі, щоб забезпечити якість світового рівня та ідеальне освітлення для всіх стилів інтер’єру'}
                ]
            }
        }
    })
</script>

<style lang="scss">
/* Slider */


.top {
    &__inner {
        margin-bottom: 7rem;
        position: relative;
        &::after {
            content: '';
            background-image: url(../assets/images/slider-top-bg.jpg);
            width: 100%;
            height: 72.2rem;
            position: absolute;
            top: 0;
            z-index: -1;
        }  
    }

    &__slider {
        &-item {
            display: flex !important;
            justify-content: center;
            align-items: center;
        }
        &-info {
            text-align: left;
            padding: 3rem;
        }
        &-img {
            max-width: 70.3rem;
            object-fit: cover;
            margin-right: 2.5rem;
            margin-left: -1.5rem;
        }
        &-title {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            font-size: 5rem;
            line-height: 4.5rem;
            color: #363838;
            position: relative;
            &::after {
                content: '';
                width: 18.5rem;
                background-color: #6d7278;
                height: 1px;
                display: block;
                margin: 2.6rem 0;
            }
        }
        &-text {
        }
    }
}


</style>