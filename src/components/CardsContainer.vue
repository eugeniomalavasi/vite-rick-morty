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
    <div class="row justify-content-center g-3 mt-3" >
      <div v-for="character in dataArray" class="col-sm-10 col-md-4 col-lg-2 d-flex justify-content-center">
        <AppCard :characterObj = "character"/>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>

</style>