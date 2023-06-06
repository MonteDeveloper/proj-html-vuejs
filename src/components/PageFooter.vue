<script>

export default {
    name: "PageFooter",
    props: {
        textListCol1: Array,
        textListCol2: Array,
        textCol3: String
    },
    data() {
        return {
        }
    },
    mounted() {
        console.log("Caricato il componente 'PageFooter'.");
    }
}
</script>

<template>
    <footer>
        <div class="d-flex flex-wrap">
            <div class="my-bgStars col-12 col-md-6 p-5">
                <div class="text-white d-flex position-relative h-100 justify-content-center align-items-center">
                    <div class="d-flex">
                        <!-- COLUMN -->
                        <div class="col-4">
                            <h2 class="h5 orangeTitle pb-3">FIND OUR RESTAURANTS</h2>
                            <p v-for="textParagraph in textListCol1" class="text-secondary">
                                <span v-for="textRow in textParagraph">{{ textRow }}<br></span>
                            </p>
                        </div>

                        <!-- COLUMN -->
                        <div class="col-4">
                            <h2 class="h5 orangeTitle pb-3">WORKING HOURS</h2>
        
                            <div v-for="textGroup in textListCol2">
                                <h3 class="h6 orangeTitle">{{textGroup.title}}</h3>
                                <p class="text-secondary" :class="{'text-danger': textGroup.dangerInfo}">{{ textGroup.info }}</p>
                            </div>
        
                            <div class="d-flex gap-3 pt-4">
                                <h3 class="h6 orangeTitle">FOLLOW US</h3>
                                <a class="fa-brands fa-twitter text-white text-underline-none text-decoration-none" target="_blank" :href="`https://twitter.com/DON_PEPPE`"></a>
                                <a class="fa-brands fa-facebook-f text-white text-underline-none text-decoration-none" target="_blank" :href="`https://it-it.facebook.com/public/DON-PEPPE`"></a>
                                <a class="fa-brands fa-instagram text-white text-underline-none text-decoration-none" target="_blank" :href="`https://www.instagram.com/DON_PEPPE`"></a>
                                <a class="fa-brands fa-linkedin-in text-white text-underline-none text-decoration-none" target="_blank" :href="`https://it.linkedin.com/company/don-peppe`"></a>
                            </div>
                        </div>
                        
                        <!-- COLUMN -->
                        <div class="col-4">
                            <p class="h3">
                                {{ textCol3 }}
                            </p>
                        </div>
                    </div>

                    <!-- ABSOLUTE POSITIONS -->
                    <p class="position-absolute start-0 bottom-0 text-secondary">
                        <span class="orangeTitle">Created with <i class="fa-regular fa-heart"></i> by</span>
                        Lorenzo Montello
                    </p>

                    <img class="position-absolute end-0 bottom-0" src="../assets/img/footer-bottom-img.png" alt="footerLogoImg">
                </div>
            </div>
            <div class="col-12 col-md-6 overflow-hidden">
                <img class="object-fit-cover" src="../assets/img/footer-img-1.jpg" alt="footerImg">
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
.orangeTitle{
    color: #b7903c;
}
</style>
