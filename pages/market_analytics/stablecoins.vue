<template>
  <div class="wrapper">
    <h2 class="inter mb-14 mt-44">Stable Coin Analysis</h2>
    <div class="w-full mb-6 flex items-end justify-between">
      <div class="flex items-end gap-2">
        <tab class="active-tab">USDT</tab>
        <tab>USDC</tab>
        <tab>BUSD</tab>
        <button class="arrow-btn">
          <img src="~/assets/images/Arrowdown.png" alt="" />
        </button>
        <span class="text-xs">More coins</span>
      </div>
      <div class="">
        <span class="text-sm font-light mr-3">USDT</span>
        <span class="text-2xl font-medium">$1.00</span>
      </div>
    </div>

   <div class="">
      <graph></graph>

      <table class="sc-table">
         <tr>
            <th>Name</th>
            <th>Chain</th>
            <th>Borrow APY</th>
            <th>Lend APY</th>
        </tr>

       <tbody>
        <tr v-for="stablecoin in stablecoins" :key="stablecoin">
          <td class="flex items-center gap-3">
            <img :src="stablecoin.img" alt="" />
            {{ stablecoin.name }}
          </td>
          <td>{{ stablecoin.chain }}</td>
          <td>{{ stablecoin.borrow_apy }}</td>
          <td>{{ stablecoin.lend_apy }}</td>
        </tr>
        <tr v-for="stablecoin in stablecoins" :key="stablecoin">
          <td class="flex items-center gap-3">
            <img :src="stablecoin.img" alt="" />
            {{ stablecoin.name }}
          </td>
          <td>{{ stablecoin.chain }}</td>
          <td>{{ stablecoin.borrow_apy }}</td>
          <td>{{ stablecoin.lend_apy }}</td>
        </tr>
        <tr v-for="stablecoin in stablecoins" :key="stablecoin">
          <td class="flex items-center gap-3">
            <img :src="stablecoin.img" alt="" />
            {{ stablecoin.name }}
          </td>
          <td>{{ stablecoin.chain }}</td>
          <td>{{ stablecoin.borrow_apy }}</td>
          <td>{{ stablecoin.lend_apy }}</td>
        </tr>
        <tr v-for="stablecoin in stablecoins" :key="stablecoin">
          <td class="flex items-center gap-3">
            <img :src="stablecoin.img" alt="" />
            {{ stablecoin.name }}
          </td>
          <td>{{ stablecoin.chain }}</td>
          <td>{{ stablecoin.borrow_apy }}</td>
          <td>{{ stablecoin.lend_apy }}</td>
        </tr>
       </tbody>
      </table>

   </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'

import Graph from '~/components/Graph.vue';

export default {
  components: { Graph },
    name: 'stablecoins',
    data() {
        return {

        }
    },

    computed: {
      stablecoins() {
        return this.$store.state.stablecoins;
      }    
  },

};
</script>

<style>
th, td {
  padding: 16px 66px !important;
}
.sc-table {
  margin-top: 2px;
  margin-bottom: 50px;
}
</style>