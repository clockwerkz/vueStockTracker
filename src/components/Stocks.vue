<template>
    <div>
        <div v-bind:key="stock.id" v-for="stock in stocks">
            <h3>{{stock.symbol}}</h3>
        </div>
    </div>  
</template>


<script>
export default {
    name: 'Stocks',
    props: ["stocks"]
}
</script>

<style scoped>

</style>