<script>
export default {
    name: 'AppFooter',

    data() {
        return {
            socials: ["/img/footer-facebook.png", "/img/footer-twitter.png", "public/img/footer-youtube.png", "public/img/footer-pinterest.png", "/img/footer-periscope.png"],
        }
    }
}
</script>

<template>
    
    <footer>
        <div>
            <a href="#">SIGN-UP NOW</a>
            <div id="socials-container">
                <p>FOLLOW US</p>
                <ul id="socials-line">
                    <li v-for="currentSocial in socials">
                        <img :src=currentSocial>
                    </li>
                </ul>
            </div>
        </div>
    </footer>

</template>

<style lang="scss">
    @use '../style/variables' as *;
    @use '../style/mixins' as *;

    footer {
        @include centered;

        height: 136px;
        width: 100%;

        background-color: #171617;

        div {
            @include maxwidthed($maxWidth);
            width: 100%;
            height: 100%;

            display: flex;
            justify-content: space-between;
            align-items: center;
            
            a {
                padding: 1em;
                border: 2px solid $primaryColor;

                white-space: nowrap;

                text-decoration: none;
                text-align: center;
                color: white;
            }

            #socials-container {
                display: flex;
                justify-content: flex-end;
                gap: 1.5em;

                p {
                    font-size: larger;
                    font-weight: 700;
                    color: $primaryColor
                }

                #socials-line {
                    display: flex;
                    gap: 1.5em;

                    li {
                        list-style: none; 
                    }
                }
            }
        }
    }
</style>