<template>
  <div class="">
    <h2 class="wrapper ma-headers lg:mb-14 mb-6">Stable Coin Analysis</h2>
    <div
      class="
        wrapper
        w-full
        mb-6
        flex
        lg:flex-row
        flex-col
        lg:items-end
        items-start
        justify-between
      "
    >
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

    <div class="sc-graph wrapper">
      <graph></graph>
    </div>

    <div class="wrapper">
      <table class="lg:table hidden">
        <tr>
          <th>Name</th>
          <th>Chain</th>
          <th>Borrow APY</th>
          <th>Lend APY</th>
        </tr>

        <tbody>
          <tr
            class="stable-cointable"
            v-for="(coin, i) in stableCoins"
            :key="i"
          >
            <td class="flex items-center gap-3">
              <img :src="`/images/${coin.img}`" alt="" />
              {{ coin.name }}
            </td>
            <td>{{ coin.chain }}</td>
            <td>{{ coin.borrow_apy }}</td>
            <td>{{ coin.lend_apy }}</td>
          </tr>
        </tbody>
      </table>
    </div>

    <div class="wrapper s-btn-holder w-full text-center">
      <NuxtLink to="/stable_coins">
        <button class="show-btn font-semi-bold lg:p-9 p-2">Show All</button>
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
    return {};
  },

  computed: {
    stableCoins() {
      return this.$store.state.stable_coins.stableCoins.slice(0, 3);
    },
  },
};
</script>

<style scoped>
th,
td {
  padding: 16px 66px !important;
}

@media screen and (max-width: 540px) {
  .s-btn-holder,
  .sc-graph {
    padding: 0px !important;
  }
}
</style>
