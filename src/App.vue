<script>
    import AppHeader from './components/AppHeader.vue';
    import CardsContainer from './components/CardsContainer.vue';
    import AppSearch from './components/AppSearch.vue';
    import { store } from './store.js';

    import axios from 'axios';
    export default {
        components: {
            AppHeader,
            CardsContainer,
            AppSearch,
        }, created() {
            this.isLoading = 'true';
            axios
                .get("https://rickandmortyapi.com/api/character")
                .then((resp) => {
                    this.store.importArray = resp.data.results;
                    this.isLoading = 'false';
                    console.log(resp);
                })
        }, data() {
            return {
                importArray: [],
                isLoading: 'true',
                store,
            }
        }, methods: {
            changeStatus() {
                console.log('status:', this.store.selectedStatus);

                const paramsObj = {
                    status: this.store.selectedStatus,
                };
                if(this.store.selectedStatus === "all") {
                    axios
                .get("https://rickandmortyapi.com/api/character")
                .then((resp) => {
                    this.store.importArray = resp.data.results;
                })
                }
                axios
                    .get("https://rickandmortyapi.com/api/character", {
                        params: paramsObj,
                    })

                    .then((response) => {
                        this.store.importArray = response.data.results;
                        console.log(response);
                    })

            }
        },
    }
</script>

<template>

    <AppHeader />

    <SearchTotal />
    <AppSearch @filter="changeStatus" />

    <CardsContainer v-if="isLoading" />
    <div v-else> caricamento </div>


</template>

<style lang="scss">

</style>