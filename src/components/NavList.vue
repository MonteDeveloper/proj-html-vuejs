<script>

export default {
    name: "NavList",
    props: {
        list: Array
    },
    data() {
        return {
        }
    },
    mounted() {
        // console.log("Caricato il componente 'NavList'.");
    }
}
</script>

<template>
    <nav class="navbar navbar-expand-lg navbar-dark">
        <div class="container-fluid">
            <ul class="navbar-nav">
                <li v-for="item in list" class="nav-item m-2">
                    <a v-if="Array.isArray(item)" class="nav-link active d-flex gap-1 align-items-center" aria-current="page">
                        <img :src="item[1]" alt="mini-logo">
                        <span>{{item[0]}}</span>
                    </a>
                    <a v-else class="nav-link active" aria-current="page">{{item}}</a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<style lang="scss" scoped>
nav {
    color: white;

    a{
        transition: transform .2s;

        &:hover{
            transform: scale(1.1);
            cursor: pointer;
        }
    }
    
    img{
        width: 1.5rem;
        filter: invert(100%); //rendo bianca l'svg
    }
}

</style>
