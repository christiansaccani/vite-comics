<script>
export default {
    name: 'AppMedia',

    data() {
        return {
            medias: [
                {
                    img: "/img/buy-comics-digital-comics.png",
                    title: "digital comics"
                },
                {
                    img: "/img/buy-comics-merchandise.png",
                    title: "dc merchandise"
                },
                {
                    img: "/img/buy-comics-subscriptions.png",
                    title: "subscription"
                },
                {
                    img: "/img/buy-comics-shop-locator.png",
                    title: "comic shop locator"
                },
                {
                    img: "/img/buy-dc-power-visa.svg",
                    title: "dc power visa"
                },
            ],
        }
    }
}
</script>

<template>
    <section id="mediaSection">
        <div>
            <ul>
                <li v-for="currentMedia in medias">
                    <img :src="currentMedia.img" alt="">
                    {{ currentMedia.title }}
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss">
    @use '../style/variables' as *;
    @use '../style/mixins' as *;

    #mediaSection {
        @include centered;

        height: 155px;
        width: 100%;

        background-color: $primaryColor;
        color: white;
        
        div {
            max-width: $maxWidth;
            width: 100%;

            font-size: medium;

            ul {
                display: flex;
                justify-content: space-around;
                align-items: center;

                li {
                    display: flex;
                    align-items: center;
                    gap: 1em;

                    list-style: none;
                    text-transform: uppercase;

                    img {
                        height: 60px;
                    }
                }
            }
        }
    }
</style>