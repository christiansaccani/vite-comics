<script>
export default {
    name: 'AppContent',
}
</script>

<template>
    <section id="contentSection">
        <img src="/img/jumbotron.jpg" alt="">
        <div>
            --> Content Goes Here <--
        </div>
    </section>
</template>

<style lang="scss">
    @use '../style/variables' as *;
    @use '../style/mixins' as *;

    #contentSection {
        @include centered;
        display: flex;
        flex-direction: column;
        align-items: center;

        width: 100%;

        background-color: #171617;
        color: white;

        img {
            width: 100%;
            height: 400px;
            object-fit: cover;
            object-position: center top;
        }

        div {
            @include maxwidthed($maxWidth);
            width: 100%;

            font-size: x-large;
            font-weight: 600;
        }
    }
</style>