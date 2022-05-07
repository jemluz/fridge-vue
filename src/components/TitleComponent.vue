<template>
    <router-link class="title" to="/">
        <h3>Minha</h3>
        <h1>Geladeira</h1>
    </router-link>
</template>

<script>
export default {
    name: 'TitleComponent'
}
</script>

<style lang="scss" scopped>
    .title {
        text-align: center;

        h1 {
            font-size: 2.4rem;
            color: #000;
            font-weight: 500;
        }

        h3 {
            font-size: 1.4rem;
            color: #000;
            font-weight: 500;
        }
    }

</style>
