<template>
    <div>
        <app-stock :key="stock.id" v-for="stock in stocks" :stock="stock" ></app-stock>
    </div>
</template>

<script>
import Stock from './Stock.vue'


export default {
    data() {
        return {
        }
    },
    components:{
        AppStock: Stock
    },
    computed: {
        stocks() {
            return this.$store.getters.stocks
        }
    }
}
</script>

<style>

</style>