<script>
export default {
    name: 'AppLinks',

    data() {
        return {
            links: [
                {
                    title: "dc comics",
                    actions: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                },
                {
                    title: "shop",
                    actions: ["Shop DC", "Shop DC Collectibles"]
                },
                {
                    title: "dc",
                    actions: ["Terms Of Us", "Privacy Policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"]
                },
                {
                    title: "sites",
                    actions: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"]
                },
            ],
        }
    }
}
</script>

<template>

    <section id="linkSection">
        <div id="link-container">
            <div>
                <ul v-for="currentTitle in links">
                    <div class="linkTitle">
                        {{ currentTitle.title }}
                    </div>
                    <li v-for="currentAction in currentTitle.actions">
                        {{ currentAction }}
                    </li>
                </ul>
            </div>
        </div>
    </section>

</template>

<style lang="scss">
    @use '../style/variables' as *;
    @use '../style/mixins' as *;

    #linkSection {
        @include centered;

        height: 370px;
        width: 100%;

        background-image: url("/img/footer-bg.jpg");

        background-size: cover;

        color: white;

        #link-container {
            max-width: $maxWidth;
            width: 100%;
            max-height: 100%;

            display: flex;
            justify-content: flex-start;

            margin-top: 40px;

            div {
                display: flex;
                flex-flow: column wrap;
                gap: 2em;
                
                ul {
                display: flex;
                flex-direction: column;
                align-items: flex-start;

                    .linkTitle {
                        font-size: large;
                        font-weight: 600;
                        text-transform: uppercase;

                        margin-bottom: .5em;
                    }

                    li {
                        font-size: small;
                        font-weight: 400;

                        list-style: none; 
                        margin-bottom: .3em;

                        color: #959595;
                    }
                }
            }            
        }
    }

</style>