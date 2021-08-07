<template>
    <div class="slide">
        <img v-bind:src="slide.src" alt="">
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