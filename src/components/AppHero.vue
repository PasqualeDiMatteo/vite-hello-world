<script>
export default {
    data() {
        return {
            img: "130-536x354.jpg"
        }
    },
    methods: {
        getImagePath(img) {
            const url = new URL(`../assets/${img}`, import.meta.url)
            return url.href
        }
    }
}
</script>

<template>
    <div>
        <img src="../assets/242-536x354.jpg" alt="Image random">
        <h2>Image with address in folder</h2>
    </div>
    <div>
        <img :src="getImagePath(img)" alt="Image random">
        <h2>Image with relative address in the folder</h2>
    </div>
</template>


<style>
div {
    text-align: center;
}
</style>