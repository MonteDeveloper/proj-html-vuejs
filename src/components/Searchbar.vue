<script>

export default {
    name: "Searchbar",
    props: {
        placeholder: String,
        imgPath: String
    },
    data() {
        return {
        }
    },
    mounted() {
        // console.log("Caricato il componente 'Searchbar'.");
    }
}
</script>

<template>
    <div class="position-relative d-flex align-items-center">
        <i class="fa-solid fa-magnifying-glass text-white m-1"></i>
        <input type="text" name="search" :placeholder="placeholder">
    </div>
</template>

<style lang="scss" scoped>
input {
    color: rgba(255, 255, 255, 0.5);
    background-color: transparent;
    border: none;
    width: 70px;

    &::placeholder{
        color: white;
    }

    &:focus-visible{
        outline: none !important;
    }
}
</style>
