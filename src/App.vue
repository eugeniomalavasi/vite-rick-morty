<script>
    import AppHeader from './components/AppHeader.vue';
    import CardsContainer from './components/CardsContainer.vue';
    import axios from 'axios';
export default {
    components: {
        AppHeader,
        CardsContainer
    }, created() {
        axios
    .get("https://rickandmortyapi.com/api/character")
        .then((resp) => {
            this.dataArray = resp.data.results;   
            console.log(resp);
        })
    }, data() {
        return {
            dataArray: [],
        }
    }
}
</script>

<template>

    <AppHeader />
    
    <CardsContainer :dataArray = "dataArray" />

</template>

<style lang="scss">
    
</style>