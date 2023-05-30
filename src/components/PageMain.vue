<script>
import SliderCarousel from './SliderCarousel.vue'

export default {
    name: "PageMain",
    components: {
        SliderCarousel
    },
    data() {
        return {
            jumboImages: [
                [
                    "../src/assets/img/h3-rev-img-1.png",
                    "../src/assets/img/h3-rev-img-2.png"
                ],
                [
                    "../src/assets/img/h3-rev-img-3.png",
                    "../src/assets/img/h3-rev-img-4.png"
                ],
                [
                    "../src/assets/img/h3-rev-img-5.png",
                    "../src/assets/img/h3-rev-img-6.png"
                ]
            ]
        }
    },
    mounted() {
        console.log("Caricato il componente 'PageMain'.");
    }
}
</script>

<template>
    <SliderCarousel :imagesList="jumboImages" :imagesWidth="[35, 13]"/>
</template>

<style lang="scss" scoped></style>
