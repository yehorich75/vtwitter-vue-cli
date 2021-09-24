<template>
    <main class="main-content">
        <div class="top">
            <div class="top__inner">
                <div class="container">
                    <carousel :items-to-show="1">                                                        
                        <carousel-slides>
                            <slide v-for="slide in slides" 
                                :key="slide.id" :id="slide.id"
                                :src="slide.src"
                                :title="slide.title"
                                :text="slide.text" 
                            />
                        </carousel-slides>
                    </carousel>
                </div>
            </div>
        </div>    
    </main>
</template>

<script>

    // import VueSlickCarousel from 'vue-slick-carousel';
    // optional style for arrows & dots
    // import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css';
    import 'vue3-carousel/dist/carousel.css';
    import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';
    import CarouselSlides from './CarouselSlides.vue';

    export default ({
        name: 'MainContent',
        components: {
            CarouselSlides
        },
        data (){
            return {
                slides: [
                    {
                        id: '1',
                        src: require('../assets/images/slider/slider-colorful-gifts.jpg'), 
                        alt: 'Slider Image 1',
                        title: 'Чудові подарунки',
                        text: 'Абсолютно нова колекція кришталевих статуеток та особливих подарунків, зроблених вручну, для елітного оздоблення інтер’єру, особливих випадків та пам’ятних подій. Capella - це бренд з новим дизайном, вражаючою красою та персоналізованими предметами.'},
                    {
                        id: '2',
                        src: require('../assets/images/slider/slider-detailed-elegance.jpg'),
                        alt: 'Slider Image 2',
                        title: 'Детальна елегантність', 
                        text: 'Наші фірмовий кришталь - це блискучі дорогоцінні камені, які піднімають ваші освітлювальні та декоративні вироби на абсолютно новий рівень чарівності.'},
                    {
                        id: '3',
                        src: require('../assets/images/slider/slider-perfect-chandeliers.jpg'),
                        alt: 'Slider Image 3',
                        title: 'Ідеальні люстри',
                        text: 'Ефектні шедеври освітлення, зроблені з найкращих матеріалів, щоб забезпечити якість світового рівня та ідеальне освітлення для всіх стилів інтер’єру'}
                ],
                slideClass: 'slide',
                slideImgClass: 'slide__img'
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
            padding: 5rem 3rem 0;
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
    }
}
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