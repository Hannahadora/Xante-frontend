<template>
  <div>
      <h2 class="inter font-medium">Stable Coin Analysis</h2>

      <div class="flex items-end justify-between mb-6 mt-14">
        <div class="flex items-end gap-2">
          <tab class="active-tab">USDT</tab>
          <tab>USDC</tab>
          <tab>BUSD</tab>
          <button class="arrow-btn"><img src="~/assets/images/Arrowdown.png" alt=""></button>
          <span class="text-xs">More coins</span>
        </div>
        <div class="">
            <span class="text-sm font-light mr-3">USDT</span>
            <span class="text-2xl font-medium">$1.00</span>
        </div>
      </div>
      <graph></graph>

      <table class="mt-1">
        <tr>
            <th>Name</th>
            <th>Price</th>
            <th>Borrow APY</th>
            <th>Lend APY</th>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/Group 30.png" alt="">
                Tether</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img class="" src="~/assets/images/Group 30 (1).png" alt="">
                USD Coin</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/Group 30 (2).png" alt="">
                Binance USD</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/HUSD.png" alt="">
               HUSD</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/Gem Dollar.png" alt="">
                Gem Dollar</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/Group 30.png" alt="">
                Tether</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img class="" src="~/assets/images/Group 30 (1).png" alt="">
                USD Coin</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/Group 30 (2).png" alt="">
                Binance USD</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/HUSD.png" alt="">
               HUSD</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/Gem Dollar.png" alt="">
                Gem Dollar</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/Group 30.png" alt="">
                Tether</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img class="" src="~/assets/images/Group 30 (1).png" alt="">
                USD Coin</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/Group 30 (2).png" alt="">
                Binance USD</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/HUSD.png" alt="">
               HUSD</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/Gem Dollar.png" alt="">
                Gem Dollar</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/Group 30.png" alt="">
                Tether</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img class="" src="~/assets/images/Group 30 (1).png" alt="">
                USD Coin</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/Group 30 (2).png" alt="">
                Binance USD</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/HUSD.png" alt="">
               HUSD</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="~/assets/images/Gem Dollar.png" alt="">
                Gem Dollar</td>
            <td>Bsc</td>
            <td>$15.0 B</td>
            <td>$15.0 B</td>
        </tr>
      </table>
  </div>
</template>

<script>
import Graph from '../Graph.vue'
import Tab from '../Tab.vue'
export default {
    name: 'StableCoin',
    components: { Graph, Tab }

       }
</script>

<style scoped>
    th, td {
       padding: 16px 66px;
    }
    tr {
        border-bottom: 1px solid #151F38;
    }
</style>