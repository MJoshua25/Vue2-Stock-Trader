<template>
  <div>
      <app-stock :key="stock.id" v-for="stock in stocks" :stock="stock" ></app-stock>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import stock from './Stock.vue';

export default {
    components: {
        appStock:stock,
    },
    computed: {
        ...mapGetters({
            stocks: 'stockPortfolio',
        })
    }
}
</script>

<style>

</style>