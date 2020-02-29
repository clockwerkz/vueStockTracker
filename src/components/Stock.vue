<template>
    <div class="stock">
        <p>{{stock.symbol}} 
            <span class="stock-price" v-bind:class="{'stock-price--down':stock.currentPrice - stock.prevPrice <= 0}">${{stock.currentPrice}}</span>
            <button @click="$emit('del-stock', stock.id)" class="del">x</button>    
        </p>
    </div>
</template>

<script>
export default {
    name: "Stock",
    props: ["stock"],
}
</script>

<style scoped>
    .stock {
        background: #f4f4f4;
        padding: 10px;
        border-bottom: 1px #ccc dotted;
    }

    .stock-price {
        color: #0B5;
    }

    .stock-price--down {
        color: #f00;
    }

    .del {
        background: #ff0000;
        color: #fff;
        border: none;
        padding: 5px 9px;
        border-radius: 50%;
        cursor: pointer;
        float: right;
    }

</style>