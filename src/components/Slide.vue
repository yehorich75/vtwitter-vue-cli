<template>
    <div class="slide">
        <img v-bind:src="slide.src" width="700">
        <!-- {{slide.src}} -->
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