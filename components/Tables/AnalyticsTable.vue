<template>
  <div>
      <graph></graph>

      <table class="lg:block hidden w-full">
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

      <div class="mobile-ma-table lg:hidden block" v-for="ma in filteredMarketAnalytics" :key="ma">
          <div class="flex items-center gap-3">
              <img :src="ma.img" alt="" />
              {{ ma.name }}
            </div>

           <div class="flex items-center justify-between">
               <span>Chain</span>
               <span>{{ ma.chain }}</span>
           </div>

           <div class="flex items-center justify-between">
               <span>Category</span>
               <span>{{ ma.category }}</span>
           </div>

           <div class="flex items-center justify-between">
               <span>Locked Value</span>
               <span>{{ ma.locked_value }}</span>
           </div>
      </div>
       <div class="w-full mx-auto text-center" style="background: #0a132b">
        <NuxtLink to="/market_analytics/analytics">
          <button class="font-semi-bold p-9">Show All</button>
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
    }
</style>