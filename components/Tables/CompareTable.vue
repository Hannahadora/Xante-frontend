<template>
  <table id="compare-table">
     <tr class="">
        <th>Platforms</th>
        <th>Categories</th>
        <th>Locked value</th>
        <th class="flex flex-col justify-flex-end">
          <div class="mb-7">
            <img src="~/assets/images/eth.png" alt="">
            <span class="text-sm">ETH</span>
          </div>
          APY
        </th>
        <th>
           <div class="mb-7">
            <img src="~/assets/images/btc.png" alt="">
            <span class="text-sm">BCH</span>
          </div>
          APY
        </th>
        <th>
           <div class="mb-7">
            <img src="~/assets/images/kcs.png" alt="">
            <span class="text-sm">KCS</span>
          </div>
          APY
        </th>
        <th>
          <div class="mb-7">
            <img src="~/assets/images/eth.png" alt="">
            <span class="text-sm">ETH</span>
          </div>
          APY
        </th>
        <th>
          <div class="mb-7">
            <img src="~/assets/images/btc.png" alt="">
            <span class="text-sm">BCH</span>
          </div>
          APY
        </th>
        <th>
          <div class="mb-7">
            <img src="~/assets/images/kcs.png" alt="">
            <span class="text-sm">KCS</span>
          </div>
          APY
        </th>
        <th></th>
      </tr>

      <tr class="" v-for="coin in coins" :key="coin">
        <td class="platform-col">
          <img :src="coin.img" alt=""> 
          {{ coin.platform }}
        </td>
        <td>
          <div class="coin_category-grid">
            <div v-for="category in coin.categories" :key="category">{{ category }}</div>
          </div>
        </td>
        <td class="lockvalue-col">{{ coin.locked_value }}<span class="lockvalue-percent">+14.81%</span> </td>
        <td>{{ coin.ETH_APY }}</td>
        <td>{{ coin.BCH_APY }}</td>
        <td>{{ coin.KCS_APY }}</td>
        <td>{{ coin.ETH_APY }}</td>
        <td>{{ coin.BCH_APY }}</td>
        <td>{{ coin.KCS_APY }}</td>
        <td><LGreenBtn/></td>
      </tr>

  </table>
</template>

<script>
import LGreenBtn from '~/components/Buttons/LGreenBtn.vue'
export default {
    name: 'CompareTable',
  components: { LGreenBtn, },
  data() {
    return {
      coins: [
        {
          platform: 'Aave', img: '~/assets/images/Aave.png', categories: [ 'DEX', 'DEX', ], locked_value: '$10.3B', ETH_APY: '23.5%', BCH_APY: '23.5%', KCS_APY: '23.5%', ETH_APY: '23.5%', BCH_APY: '23.5%', KCS_APY: '23.5%',
          platform: 'Binance', img: '~/assets/images/Binance.png', categories: [ 'ETH', 'AMM', 'All Chains' ], locked_value: '$10.3B', ETH_APY: '23.5%', BCH_APY: '23.5%', KCS_APY: '23.5%', ETH_APY: '23.5%', BCH_APY: '23.5%', KCS_APY: '23.5%',
          platform: 'compound', img: '~/assets/images/Compound.png', categories: [ 'DEX', 'DEX', ], locked_value: '$10.3B', ETH_APY: '23.5%', BCH_APY: '23.5%', KCS_APY: '23.5%', ETH_APY: '23.5%', BCH_APY: '23.5%', KCS_APY: '23.5%',
        }
      ]
    }
  }
}
</script>

<style scoped>

    #compare-table 
      tr {
            border-bottom: 1px solid #151F38;

        }
      td {
          padding: 19px 20px;
      }
      
      th {
        padding: 19px 20px;
        /* text-align: left; */
        vertical-align: bottom;
      }

</style>