<template>
  <div class="">
    <h2 class="wrapper ma-headers lg:mb-14 mb-6">Stable Coin Analysis</h2>
    <div class="wrapper w-full mb-6 flex lg:flex-row flex-col lg:items-end items-start justify-between">
      <div class="flex items-end gap-2">
        <tab class="active-tab">USDT</tab>
        <tab>USDC</tab>
        <tab>BUSD</tab>
        <button class="arrow-btn">
          <img src="~/assets/images/Arrowdown.png" alt="" />
        </button>
        <span class="text-xs lg:block hidden">More coins</span>
      </div>

      <div class="flex items-center lg:mt-0 mt-4">
        <span class="lg:text-sm small-text font-light mr-3">USDT</span>
        <h5 class="inter lg:text-2xl text-sm">$1.00</h5>
      </div>
    </div>

    <div class="">
       <graph> </graph>
    </div>

      <table class="wrapper lg:block hidden">
        <tr>
          <th>Name</th>
          <th>Chain</th>
          <th>Borrow APY</th>
          <th>Lend APY</th>
        </tr>

        <tbody>
          <tr
            class="stable-cointable"
            v-for="stablecoin in filteredstablecoins"
            :key="stablecoin"
          >
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

        <div class="wrapper w-full mx-auto text-center" style="background: #0a132b">
        <NuxtLink to="/market_analytics/stablecoins">
          <button class="font-semi-bold lg:p-9 p-2">Show All</button>
        </NuxtLink>
      </div>
  </div>
</template>

<script>
import Graph from "../Graph.vue";
import Tab from "../Tab.vue";

export default {
  name: "StableCoinTable",
  components: { Graph, Tab },
  data() {
    return {
      
    };
  },

  computed: {
    stablecoins() {
      return this.$store.state.stablecoins;
    },
    filteredstablecoins() {
      return this.$store.getters.filteredstablecoins
    },
  },
};
</script>

<style scoped>

th, td {
  padding: 16px 66px !important;
}

</style>