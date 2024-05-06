<script>
    export default {
        props: {
            characterObj: Object,
        },
        data() {
            return {

            }
        }, methods: {
        },
    }
</script>

<template>
    <div>
        <img :src="characterObj.image" alt="">
        <p>{{ characterObj.name }}</p>
        <p>{{ characterObj.status }}</p>
        <p>{{ characterObj.species
        }}</p>
    </div>
</template>

<style lang="scss" scoped>
    img {
        max-width: 100%;
        height: 150px;
        width: 150px;
        border-radius: 50%;
        box-shadow: 5px 5px 5px black;
    }
</style>