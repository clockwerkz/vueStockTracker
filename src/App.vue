<template>
  <div id="app">
    <Stocks v-bind:stocks="stocks"/>
  </div>
</template>

<script>
import Stocks from './components/Stocks';
export default {
  name: 'App',
  components: {
    Stocks
  },
  data() {
    return {
      stocks: [
        {
          id: 1,
          symbol: 'ATVI',
          currentPrice: 45
        },
        {
          id: 2,
          symbol: 'DIS',
          currentPrice: 110
        },
        {
          id: 1,
          symbol: 'MSFT',
          currentPrice: 161
        },
      ]
    }
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }

</style>
