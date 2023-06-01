<script>

export default {
    name: "CardPerson",
    props: {
        imgPath: String,
        name: String,
        description: String,
        cardBackColor: String
    },
    data() {
        return {
            crimson: 'crimson'
        }
    },
    mounted() {
        // console.log("Caricato il componente 'CardPerson'.");
    }
}
</script>

<template>
    <!-- <div class="my-card overflow-hidden position-relative">
        <img class="img-fluid" :src="imgPath" alt="CardPerson-img">

    </div> -->
    <div class="my-card position-relative overflow-hidden">
        <div class="flip-card">
            <div class="flip-card-inner">
                <div class="flip-card-front">
                    <img class="img-fluid" :src="imgPath" alt="CardPerson-img">
                </div>
                <div class="flip-card-back d-flex flex-column justify-content-center" :style="`background-color: ${cardBackColor}`">
                    <h3>{{ name }}</h3>
                    <p>{{ description }}</p>
                    <div class="d-flex justify-content-center">
                        <div class="d-flex gap-2">
                            <a class="fa-brands fa-instagram text-white text-underline-none text-decoration-none" target="_blank" :href="`https://www.instagram.com/${name.replace(' ', '')}`"></a>
                            <a class="fa-brands fa-twitter text-white text-underline-none text-decoration-none" target="_blank" :href="`https://twitter.com/${name.replace(' ', '_')}`"></a>
                            <a class="fa-brands fa-facebook-f text-white text-underline-none text-decoration-none" target="_blank" :href="`https://it-it.facebook.com/public/${name.replace(' ', '-')}`"></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <img class="position-absolute top-50 start-50 translate-middle pe-none" src="../assets/img/square-pattern.png" alt="bg-img">
    </div>
</template>

<style lang="scss" scoped>
// .my-card {
//     SquarePatternBackground{
//         border: 2px solid crimson;
//     }
//     img {
//         object-fit: cover;
//         transition: opacity .2s, scale .2s;
//         opacity: 1;
//         scale: 1;
//     }

//     img.my-hovered{
//         z-index: -1;
//         width: 150%;
//     }

//     .my-hovered {
//         transition: opacity .2s;
//         opacity: 0;
//     }

//     &:hover {
//         cursor: pointer;

//         img {
//             transition-delay: .5s;
//             opacity: 0;
//             scale: 1.2;
//         }

//         .my-hovered {
//             transition-delay: .5s;
//             opacity: 1;
//         }

//         img.my-hovered{
//             opacity: .4;
//         }
//     }

//     .fa-eye {
//         background-color: #d2401e;
//     }
// }

.my-card{
    & > img{
        z-index: -1;
        opacity: .4;
    }
}

.flip-card {
    background-color: transparent;
    aspect-ratio: 1/1;
    perspective: 1000px;
}

.flip-card-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: transform .6s;
    transform-style: preserve-3d;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
}

.flip-card:hover .flip-card-inner {
    transition-delay: 1s;
    transform: rotateY(180deg) scale(.9);
}

.flip-card-front,
.flip-card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
}

.flip-card-back {
    color: white;
    transform: rotateY(180deg);
}
</style>
