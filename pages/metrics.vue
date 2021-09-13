<template>
  <div>
    <header-vue />
    <div class="metric-view">
      <div class="wrapper">
        <h2 class="ma-headers mb-7">Compare Coins</h2>
        <span class="text-sm mb-4">Type in coin to compare</span>
      </div>

      <div class="table-div">
        <table class="metric-table">
          <tr>
            <th></th>
            <th>
              <div
                class="lg:flex flex-col items-center justify-center lg:gap-9"
              >
                <img
                  class="lg:w-auto w-5"
                  src="/images/Group 30 (1).png"
                  alt=""
                />
                <span class="lg:block hidden">{{ coinOne.name }}</span>
              </div>
            </th>
            <th>
              <div
                class="lg:flex flex-col items-center justify-center lg:gap-9"
              >
                <img class="lg:w-auto w-5" src="/images/Group 30.png" alt="" />
                <span class="lg:block hidden">{{ coinTwo.name }}</span>
              </div>
            </th>
          </tr>
          <tbody>
            <tr>
              <td>Price</td>
              <td>{{ coinOne.price }}</td>
              <td>{{ coinTwo.price }}</td>
            </tr>
            <tr>
              <td>Market Cap</td>
              <td>{{ coinOne.marketCap }}</td>
              <td>{{ coinTwo.price }}</td>
            </tr>
            <tr>
              <td>Trading Volume</td>
              <td>{{ coinOne.tradingVolume }}</td>
              <td>{{ coinTwo.tradingVolume }}</td>
            </tr>
            <tr>
              <td>Available Supply</td>
              <td>{{ coinOne.availableSupply }}</td>
              <td>{{ coinTwo.availableSupply }}</td>
            </tr>
            <tr>
              <td>All Time High</td>
              <td>{{ coinOne.allTimeHigh }}</td>
              <td>{{ coinTwo.allTimeHigh }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
import HeaderVue from "~/components/Header.vue";

export default {
  name: "metrics",
  components: {
    HeaderVue,
  },

  computed: {
    coinOne() {
      return this.$store.state.metrics.coinOne;
    },
    coinTwo() {
      return this.$store.state.metrics.coinTwo;
    },
  },
};
</script>

<style scoped>
.metric-view {
  margin-top: 154px;
  margin-bottom: 82px;
}
td {
  padding-left: 107px;
}
.table-div {
  margin: 80px 120px;
}

@media screen and (max-width: 540px) {
  td,
  th {
    padding: 20px !important;
  }
  .table-div {
    margin: 80px 0px !important;
  }
}
</style>
