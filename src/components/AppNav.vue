<script>
export default {
    name: 'AppNav',

    data() {
        return {
            links: [
                'characters',
                'comics',
                'movies',
                'tv',
                'games',
                'collectibles',
                'videos',
                'fans',
                'news',
                'shop',
            ],
        }
    }
}
</script>

<template>

    <nav>
        <div id="nav-container">
            <img id="logo" src="/img/dc-logo.png">
            <div id="menu">
                <ul>
                    <li v-for="currentLink in links">
                        {{ currentLink }}
                    </li>
                </ul>
            </div>
        </div>
    </nav>

</template>

<style lang="scss">
    @use '../style/variables' as *;
    @use '../style/mixins' as *;

    nav {
        @include centered;

        background-color: #ffffff;
        width: 100%;
        height: 120px;

        #nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;

            max-width: 1280px;
            width: 100%;
            height: 100%;

            color: black;

            #menu {
                height: 100%;

                    ul {
                    height: 100%;
                    display: flex;
                    justify-content: flex-end;
                    gap: 1em;

                    font-weight: 500;

                    li {
                        height: 100%;
                        list-style: none;
                        text-transform: uppercase;
                        vertical-align: center;
                    }
                }
            }

            
        }
    }
</style>