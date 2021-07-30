<template>
    <main class="main-content">
        <div class="top">
            <div class="top__inner">
            </div>
            <SlickCarousel />
        </div>    
    </main>
</template>

<script>

    import SlickCarousel from './SlickCarousel.vue';

    export default ({
        name: 'MainContent',
        components: {
            SlickCarousel
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
                        ext: 'Deep v you probably havent heard of them banh mi synth actually affogatAesthetic lyft ethical drinking vinegar austint'},
                    {
                        id: '3',
                        image: 'slider-perfect-chandeliers.jpg',
                        alt: 'Slider Image 3',
                        title: 'Ідеальні люстри',
                        text: 'Deep v you probably havent heard of them banh mi synth actually affogatAesthetic lyft ethical drinking vinegar austint'}
                ]
            }
        }
    })
</script>

<style scoped>
/* Slider */

.top__inner {
    margin-bottom: 7rem;
    position: relative;  
}

.top__inner::after {
    content: '';
    background-image: url(../assets/images/slider-top-bg.jpg);
    width: 100%;
    height: 72.2rem;
    position: absolute;
    top: 0;
    z-index: -1;
}

.top__slider-item {
    display: flex !important;
    justify-content: center;
    align-items: center;
}

.top__slider-info {
    max-width: 64.5rem;
}

.top__slider-img {
    max-width: 70.3rem;
    object-fit: cover;
    margin-right: 2.5rem;
    margin-left: -1.5rem;
}

.top__slider-title {
    font-family: 'Montserrat', sans-serif;
    font-weight: 700;
    font-size: 11rem;
    line-height: 13.5rem;
    color: #363838;
    position: relative;
}

.top__slider-title::after {
    content: '';
    width: 18.5rem;
    background-color: #6d7278;
    height: 1px;
    display: block;
    margin: 2.6rem 0;
}

.top__slider-text {
    max-width: 58.5rem;
}

.slick-list {
    margin-bottom: 10rem;
}
</style>