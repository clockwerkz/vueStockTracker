<template>
    <div>
        <Header />
        <div v-bind:key="stock.id" v-for="stock in stocks">
            <Stock v-bind:stock="stock" v-on:del-stock="$emit('del-stock', stock.id)"/>
        </div>
    </div>  
</template>


<script>
import Stock from './Stock';
import Header from './layout/Header';
export default {
    name: 'Stocks',
    components: {
        Stock,
        Header
    },
    props: ["stocks"]
}
</script>

<style scoped>

</style>