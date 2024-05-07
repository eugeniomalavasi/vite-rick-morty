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
    <select @change="$emit('filter')" v-model="store.selectedStatus">
        <option v-for="curStatus in status" :value="curStatus">{{ curStatus }}</option>
    </select>
</template>

<style lang="scss" scoped>

</style>