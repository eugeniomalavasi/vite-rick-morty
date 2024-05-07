<script>
    import {store} from '../store.js';
    import SearchTotal from './SearchTotal.vue';
    
    export default {
        data() {
            return {
                status: ["all","alive", "dead", "unknown"],
                store
            }
        }, components: {
            SearchTotal,
        }
    }
</script>

<template>
    <div class="filter_bar d-flex justify-content-around">
        <select @change="$emit('filter')" v-model="store.selectedStatus">
            <option v-for="curStatus in status" :value="curStatus">{{ curStatus }}</option>
        </select>
        <SearchTotal />
    </div>
</template>

<style lang="scss" scoped>
    .filter_bar {
        margin: 0 auto;
        width: 80%;
    }
</style>