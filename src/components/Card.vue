<template>
    <figure class="card">
        <img :src="singleComic.thumb" :alt="singleComic.series">
        <figcaption>{{singleComic.series}}</figcaption>
    </figure>
</template>

<script>
export default {
    name: "Card",
    props: ["singleComic"]
}
</script>

<style lang="scss" scoped>
    .card {
        width: 15%;
        margin-bottom: 50px;

        img {
            height: 200px;
            width: 100%;
            object-fit: cover;
            object-position: top;
        }
        figcaption {
            text-transform: uppercase;
            margin-top: 20px;
        }
    }
</style>