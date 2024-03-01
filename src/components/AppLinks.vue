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

            <img src="/img/dc-logo-bg.png" alt="">
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
            position: relative;

            @include maxwidthed($maxWidth);
            width: 100%;
            max-height: 100%;

            display: flex;
            justify-content: space-between;

            padding-top: 24px;

            overflow: hidden;

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

            img {
                position: absolute;
                right: 0;
                top: 50%;
                transform: translateY(-52.5%);
                height: 140%;
            }
   
        }
    }

</style>