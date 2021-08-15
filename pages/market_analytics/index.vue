<template>
  <div id="market-view">
      
      <AnalyticsTable />

      <!-- *************************STABLE COINS******************************** -->

      <div class="lg:mt-44 mt-11">
        <StableCoinsTable />    
      </div>
      

      <!-- **********************************Top 10 and 20 **************************** -->

      <div id="ma_tops" class="w-full">
        <div class="lg:w-1/2 w-full">
          <Top10 />
        </div>

        <div class="lg:w-1/2 w-full">
          <Top-20 />
        </div>
      </div>

      <!-- ********************************COMPARE COINS WITH METRICS*********************** -->

      <div class="lg:mb-12 mb-4 lg:mt-28 mt-8">
        <CompareMetricsTable />
      </div>

      <!-- ******************COIN**************************** -->

      <div class="wrapper lg:block hidden">
        <Coins />
      </div>

      <div class="marketCoinPrice-sect lg:mt-28 mt-12">   
        <CoinPrice />
      </div>

      <div class="wrapper">
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
import Coins from "~/components/Tables/Coins.vue";
import Color from "~/components/Color.vue";
import CoinPrice from "~/components/Tables/CoinPrice.vue";
// import ProviderDropdown from '~/components/providerDropdown.vue'
import Top10 from "~/components/Tables/Top10.vue";
import Top20 from "~/components/Tables/Top20.vue";
import StableCoinsTable from '~/components/Tables/StableCoinsTable.vue';
import AnalyticsTable from '~/components/Tables/AnalyticsTable.vue';
import CompareMetricsTable from '~/components/Tables/CompareMetricsTable.vue';
import DGreenBtn from '~/components/Buttons/DGreenBtn.vue';

export default {
  name: "MarketAnalytics",
  components: {
    Coins,
    Color,
    Top10,
    Top20,
    CoinPrice,
    StableCoinsTable,
    AnalyticsTable,
    CompareMetricsTable,
    DGreenBtn,
  },


  data() {
    return {
    };
  },

  methods: {

  },
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

#ma_tops {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  gap: 32px;
  padding: 0px 120px;
}

.stable-coin-table td,
th {
  padding: 16px 66px;
}


@media screen and (max-width: 1024px) {
  #ma_tops {
    padding: 0 24px;
    gap: 32px;
  }
}

@media screen and (max-width: 768px) {
  #ma_tops {
    display: block;
    padding: 0;
    gap: 0px;
  }

  .rect_14 {
    display: none;
  }
}
</style>