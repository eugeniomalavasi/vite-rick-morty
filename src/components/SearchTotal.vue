<script>
    import {store} from '../store.js';

export default {
    data() {
        return {
            store,
        }
    },
}
</script>

<template>
    <div>
        <p>personaggi selezionati: {{ store.importArray.length }}</p>
    </div>
</template>

<style lang="scss" scoped>
    
</style>