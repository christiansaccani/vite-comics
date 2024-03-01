<script>
export default {
    name: 'ComicItem',

    props: {
        comicName: String,
        comicImage: String
    },

    data() {
    },
}
</script>

<template>

    <div class="comic">
        <img :src="comicImage" :alt="comicName">
        <p>{{ comicName }}</p>
    </div>

</template>

<style lang="scss">

.comic {
    max-width: 190px !important;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;

    gap: .5em;

    img {
        height: 190px !important;
        object-fit: contain;
    }

    p{
        font-size: small;
        text-transform: uppercase;
    }
}

</style>