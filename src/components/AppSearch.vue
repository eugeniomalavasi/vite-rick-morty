<script>
    import {store} from '../store.js';
    
    export default {
        data() {
            return {
                status: ["Alive", "dead", "unknown"],
                store
            }
        },
    }
</script>

<template>
    <div class="filter_bar">
        <select @change="$emit('filter')" v-model="store.selectedStatus">
            <option v-for="curStatus in status" :value="curStatus">{{ curStatus }}</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
    .filter_bar {
        margin: 0 auto;
        width: 80%;
    }
</style>