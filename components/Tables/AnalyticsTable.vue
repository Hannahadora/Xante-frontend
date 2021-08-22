<template>
    <div>
      <h2 class="wrapper ma-headers mt-20">Market Analytics</h2>

      <div class="wrapper mt-12 lg:flex block items-center justify-between wrapper">
        <div class="flex items-start">
          <div
            class="h-14 flex items-center gap-2 mr-4"
            style="background: #1f2b4a"
          >
            <p class="py-3 px-5 m-1 rounded" style="background: #056237">
              Locked Value
            </p>
            <p class="py-3 px-5">Stable coin Analysis</p>
            <plus-icon class="m-1" />
          </div>
          <!-- <ProviderDropdown /> -->
        </div>

        <div class="lg:flex hidden items-center gap-2">
          <tab class="active-tab">ALL</tab>
          <tab>DEFI</tab>
          <tab>NFT</tab>
          <tab>HECO</tab>
        </div>
      </div>

      <div class="wrapper lg:mt-10 mt-20 mb-4 flex items-end lg:justify-start justify-end lg:gap-12">
       <div>
          <div class="flex items-center gap-2">
            <Color theme="yellow" />
            <h5 class="inter lg:text-2xl text-xs">$92.88B</h5>
          </div>
          <span class="small-text ml-4 lg:text-sm font-light">Gross value locked</span>
        </div>
        <div>
          <div class="flex items-center gap-2">
            <Color theme="green" />
            <h5 class="inter lg:text-2xl text-xs">$92.88B</h5>
          </div>
          <span class="small-text ml-4 lg:text-sm font-light">Net value locked</span>
        </div>
      </div>


      <div class="wrapper">

          <graph ></graph>


          <table class="lg:table hidden w-full">
          <tr>
            <th>Name</th>
            <th>Chain</th>
            <th>Category</th>
            <th>Locked value</th>
          </tr>

          <tbody>
            <tr class="" v-for="(ma, i) in filteredMarketAnalytics" :key="i">
              <td class="flex items-center gap-4">
                <img :src="ma.img" alt="" />
                {{ ma.name }}
              </td>
              <td>{{ ma.chain }}</td>
              <td>
                <div class="coin_category-grid">
                  <div
                    class="coin-category"
                    v-for="(category,j) in ma.category"
                    :key="j"
                  >
                    {{ category }}
                  </div>
                </div>
              </td>
              <td>{{ ma.locked_value }}</td>
            </tr>
          </tbody>
        </table>
        <div class="lg:block hidden w-full text-center">
          <NuxtLink to="/market_analytics/analytics">
            <button class="show-btn font-semi-bold lg:p-9 p-2">Show All</button>
          </NuxtLink>
        </div>
      </div>


      <div class="mt-11 lg:hidden block">
        <div class="mobile-ma-table" v-for="(ma, i) in filteredMarketAnalytics" :key="i">
          <div class="flex items-center gap-3 mb-5">
              <img :src="ma.img" alt="" class="w-10 h-10" />
              {{ ma.name }}
            </div>

           <div class="flex items-center justify-between mb-4">
               <span>Chain</span>
               <span>{{ ma.chain }}</span>
           </div>

           <div class="flex items-center justify-between mb-4">
               <span>Category</span>
               <span>{{ ma.category }}</span>
           </div>

           <div class="flex items-center justify-between mb-4">
               <span>Locked Value</span>
               <span>{{ ma.locked_value }}</span>
           </div>
        </div>
       <div class="w-full text-center">
          <NuxtLink to="/market_analytics/analytics">
            <button class="show-btn font-semi-bold lg:p-9 p-2">Show All</button>
          </NuxtLink>
        </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'AnalyticsTable',

    data() {
     return {
        marketAnalytics: "",
     }
    },

    mounted() {
     this.marketAnalytics = this.$store.state.MarketAnalytics;
    },

    computed: {
     filteredMarketAnalytics() {
        return this.$store.getters.filteredMarketAnalytics;
     }
    }
}

</script>

<style scoped>
    table {
        margin-top: 2px;
    }

    th, td {
      padding: 16px 66px;
    }

    .mobile-ma-table {
        padding: 16px 24px 29px 24px;
        background: #0A132A;
        margin-bottom: 4px;
    }

     @media screen and (max-width: 768px) {
    h5 {
      font-size: 12px  !important;
    }

    .small-text {
      font-size: 9px;
    }

    p {
      font-size: 12px;
    }
  }

   @media screen and (max-width: 280px) {
     p {
       font-size: 10px;
     }

     h5 {
      font-size: 10px  !important;
    }

    .small-text {
      font-size: 7px;
    }
   }
</style>
