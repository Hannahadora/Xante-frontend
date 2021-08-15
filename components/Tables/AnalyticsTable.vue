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
        <graph></graph>
      </div>

      <table class="wrapper lg:block hidden w-full">
        <tr>
          <th>Name</th>
          <th>Chain</th>
          <th>Category</th>
          <th>Locked value</th>
        </tr>

        <tbody>
          <tr class="" v-for="ma in filteredMarketAnalytics" :key="ma">
            <td class="flex items-center gap-3">
              <img :src="ma.img" alt="" />
              {{ ma.name }}
            </td>
            <td>{{ ma.chain }}</td>
            <td>
              <div class="coin_category-grid">
                <div
                  class="coin-category"
                  v-for="category in ma.category"
                  :key="category"
                >
                  {{ category }}
                </div>
              </div>
            </td>
            <td>{{ ma.locked_value }}</td>
          </tr>
        </tbody>
      </table>

      <div class="mt-11">
        <div class="mobile-ma-table lg:hidden block" v-for="ma in filteredMarketAnalytics" :key="ma">
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
      </div>
       <div class="w-full mx-auto text-center" style="background: #0a132b">
        <NuxtLink to="/market_analytics/analytics">
          <button class="font-semi-bold lg:p-9 p-2">Show All</button>
        </NuxtLink>
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