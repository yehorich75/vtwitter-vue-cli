<template>
    <div class="slide">
        <img :src="slide.src" :alt="slide.alt">
        <!-- In slide with href {{ slide.src }} -->
    </div>
</template>

<script>
    export default {
        data () {
            return {}
        },
        props: {
            slide: ['slide']
        }
    }
</script>

<style lang="scss" scoped>

.slide {
    display: inline-block;
    img {
        max-width: 100%;
    }
}


</style>