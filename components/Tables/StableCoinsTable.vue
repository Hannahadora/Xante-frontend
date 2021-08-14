<template>
  <div class="">
    <h2 class="ma-headers mb-14">Stable Coin Analysis</h2>
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
          <div class="flex items-center">
            <span class="text-sm font-light mr-3">USDT</span>
            <h5 class="inter">$1.00</h5>
          </div>
        </div>

        <graph> </graph>

        <table>
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