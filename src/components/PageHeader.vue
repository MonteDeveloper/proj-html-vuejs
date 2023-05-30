<script>
import NavList from './NavList.vue'
import Searchbar from './Searchbar.vue'

export default {
    name: "PageHeader",
    components: {
        NavList,
        Searchbar
    },
    props: {
        textButton: String,
        middleNavList: Array,
        sideNavList: Array,
        logoPath: String,
        headerHeight: Number
    },
    data() {
        return {
            isOnTopPage: true
        }
    },
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
        console.log("Caricato il componente 'PageHeader'.");
    },
    methods: {
        getHalfSplittedArray(arr) {
            const firstHalf = arr.slice(0, Math.floor(arr.length / 2));
            const secondHalf = arr.slice(Math.floor(arr.length / 2));
            return [firstHalf, secondHalf];
        },
        handleScroll(event) {
            if (window.scrollY == 0) {
                this.isOnTopPage = true;
            } else {
                this.isOnTopPage = false;
            }
        }
    }
}
</script>
<template>
    <header class="fixed-top" :class="{ 'my-headerScrolled': !isOnTopPage }" :style="`height:${headerHeight}px`">
        <div class="my-container d-flex justify-content-between align-items-center p-3 h-100">
            <!-- LEFT SIDE-->
            <button v-if="textButton" class="my-orangeBtn">{{ textButton }}</button>

            <!-- CENTER -->
            <div class="h-100 d-flex">
                <NavList v-if="middleNavList" :list="getHalfSplittedArray(middleNavList)[0]" />
                <img class="h-100" v-if="logoPath" :src="logoPath" alt="logo_donPeppe">
                <NavList v-if="middleNavList" :list="getHalfSplittedArray(middleNavList)[1]" />
            </div>

            <!-- RIGHT SIDE -->
            <div class="d-flex">
                <NavList v-if="sideNavList" :list="sideNavList" />
                <Searchbar placeholder="SEARCH" />
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    transition: background-color .4s;
    font-size: .8em;

    .my-headerScrolled {
        background-color: #212529;
    }
}
</style>
