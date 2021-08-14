<template>
  <div>
    <div id="market-view" class="">
      
      <AnalyticsTable />

      <!-- *************************STABLE COINS******************************** -->

      <div class="mt-44">
        <StableCoinsTable />    
      </div>
      

      <!-- **********************************Top 10 and 20 **************************** -->

      <div id="ma_tops">
        <div class="lg:w-1/2 w-full">
          <Top10 />
        </div>

        <div class="lg:w-1/2 w-full">
          <Top-20 />
        </div>
      </div>

      <!-- ********************************COMPARE COINS WITH METRICS*********************** -->

      <h2 class="font-medium ma-headers mb-12 mt-28">Compare coins</h2>
      <table id="ma_table06" class="mb-24">
        <tr>
          <td rowspan="2" class="inter">
            <h5>
              Compare coins different <br />
              coins using varieties of <br />
              metrics
            </h5>
          </td>
          <td>
            <img class="w-12 h-12" src="./images/Group 30 (1).png" alt="" />
          </td>
          <td>
            <img class="w-12 h-12" src="./images/Group 30.png" alt="" />
          </td>
        </tr>
        <tr>
          <td>Bitcoin</td>
          <td>Ethereum</td>
        </tr>
        <tr>
          <td>
            <NuxtLink to="/market_analytics/metrics">
              <DGreenBtn text="Compare" />
            </NuxtLink>
          </td>
          <td>$15.0.B</td>
          <td>$15.0.B</td>
        </tr>
      </table>

      <!-- ******************COIN**************************** -->

      <Coins />

      <div class="marketCoinPrice-sect mt-28">   
        <CoinPrice />
      </div>

      <div class="rect_14 mt-24">
        <div class="bg_11">
          <img src="./images/Group 11.png" alt="" />
        </div>
        <div>
          <h5>
            Get access to<br />
            deeper market insight<br />
            when you join us
          </h5>
          <DGreenBtn class="mt-6" text="Join Now" />
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import DGreenBtn from "~/components/Buttons/DGreenBtn.vue";
import Coins from "~/components/Tables/Coins.vue";
import Color from "~/components/Color.vue";
import Footer from "~/components/Footer.vue";
import Graph from "~/components/Graph.vue";
import Header from "~/components/Header.vue";
import CoinPrice from "~/components/Tables/CoinPrice.vue";
// import ProviderDropdown from '~/components/providerDropdown.vue'
import Tab from "~/components/Tab.vue";
import Top10 from "~/components/Tables/Top10.vue";
import Top20 from "~/components/Tables/Top20.vue";
import StableCoinsTable from '~/components/Tables/StableCoinsTable.vue';
import AnalyticsTable from '~/components/Tables/AnalyticsTable.vue';

import { mapState } from "vuex";


export default {
  components: {
    Header,
    Footer,
    DGreenBtn,
    Coins,
    Color,
    Graph,
    Top10,
    Top20,
    CoinPrice,
    Tab,
    StableCoinsTable,
    AnalyticsTable,
  },
  name: "MarketAnalytics",

  data() {
    return {
      marketAnalytics: "",
    };
  },

  mounted() {
    this.marketAnalytics = this.$store.state.MarketAnalytics;
  },

  computed: {
    filteredMarketAnalytics() {
      return this.$store.getters.filteredMarketAnalytics;
    },
  },

  methods: {},
};
</script>

<style scoped>
#market-view {
  margin-top: 150px !important;
  margin-bottom: 130px !important;
}

table {
  margin-top: 2px;
}

.bg_11 {
  height: 273px;
  width: 326px;
  border-radius: 10px;
  background: #151f38;
  padding: 27px 30px;
  margin-right: 345px;
}

.rect_14 {
  width: 100%;
  height: 352px;
  padding: 39px 66px;
  background: #0a132b;
  display: flex;
  align-items: center;
}

#ma_table06 td {
  padding-left: 107px;
}
#ma_table06 tr {
  border: none;
}

#ma_tops {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  gap: 32px;
}

.stable-coin-table td,
th {
  padding: 16px 66px;
}


@media screen and (max-width: 768px) {
  #ma_tops {
    display: block;
  }

  .rect_14 {
    display: none;
  }
}
</style>