<script>

export default {
    name: "CardViewMore",
    props: {
        imgPath: String
    },
    data() {
        return {
        }
    },
    mounted() {
        // console.log("Caricato il componente 'CardViewMore'.");
    }
}
</script>

<template>
    <div class="my-card overflow-hidden position-relative">
        <img class="w-100" :src="imgPath" alt="CardViewMore-img">
        <div class="my-hovered position-absolute top-50 start-50 translate-middle pe-none">
            <i class="fa-regular fa-eye fs-3 p-4 rounded-circle text-white"></i>
        </div>
        <img class="my-hovered position-absolute top-50 start-50 translate-middle" src="../assets/img/square-pattern.png" alt="">
    </div>
</template>

<style lang="scss" scoped>
.my-card {
    SquarePatternBackground{
        border: 2px solid crimson;
    }
    img {
        transition: opacity .2s, scale .2s;
        opacity: 1;
        scale: 1;
    }

    img.my-hovered{
        z-index: -1;
        width: 150%;
    }

    .my-hovered {
        transition: opacity .2s;
        opacity: 0;
    }

    &:hover {
        cursor: pointer;
        
        img {
            transition-delay: .5s;
            opacity: 0;
            scale: 1.2;
        }

        .my-hovered {
            transition-delay: .5s;
            opacity: 1;
        }

        img.my-hovered{
            opacity: .4;
        }
    }

    .fa-eye {
        background-color: #d2401e;
    }
}
</style>
