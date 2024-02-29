<script>
export default {
    name: 'AppContent',
}
</script>

<template>
    <section>
        <div>
            --> Content Goes Here <--
        </div>
    </section>
</template>

<style lang="scss">
    @use '../style/variables' as *;
    @use '../style/mixins' as *;

    section {
        @include centered;
        

        height: 130px;
        width: 100%;

        background-color: #171617;
        color: white;

        div {
            max-width: $maxWidth;
            width: 100%;

            font-size: x-large;
            font-weight: 600;
        }
    }
</style>