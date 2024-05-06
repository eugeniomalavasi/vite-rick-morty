<script>
import AppCard from './AppCard.vue';

export default {
    components: {
        AppCard,
    },
    props: {
        dataArray: Array,
    },
}
</script>

<template>
<div class="container">
    <div class="row row-cols-4">
      <div class="col" v-for="character in dataArray">
        <AppCard :characterObj = "character" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>

</style>