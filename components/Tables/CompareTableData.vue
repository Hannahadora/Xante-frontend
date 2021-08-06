<template>
  <table id="compare-table">
      <tr>
        <td class="platform-col">
            <img src="~/assets/images/Aave.png" alt="">
            Aave</td>
        <td>
            <div class="coin_category-grid">
                <div class="coin-category-card">Ethereum</div>
                <div class="coin-category-card">AMM</div>
                <div class="coin-category-card">All Chains</div>
            </div>
        </td>
        <td class="lockvalue-col">$10.3B <span class="lockvalue-percent">+14.81%</span> </td>
        <td>23.5%</td>
        <td>23.5%</td>
        <td>23.5%</td>
        <td>23.5%</td>
        <td>23.5%</td>
        <td>23.5%</td>
        <td><LGreenBtn/></td>
      </tr>

      <tr>
        <td class="platform-col">
            <img src="~/assets/images/Binance.png" alt="">
            Binanace</td>
        <td>
            <div class="coin_category-grid">
                <div class="coin-category-card">DEX</div>
            </div>
        </td>
        <td class="lockvalue-col">$10.3B <span class="lockvalue-percent">+14.81%</span> </td>
        <td>23.5%</td>
        <td>23.5%</td>
        <td>23.5%</td>
        <td>23.5%</td>
        <td>23.5%</td>
        <td>23.5%</td>
        <td><LGreenBtn/></td>
      </tr>

      <tr>
          <td class="platform-col">
              <img src="~/assets/images/Compound.png" alt="">
              Compound</td>
            <td>
                <div class="coin_category-grid">
                    <div class="coin-category-card">DEX</div>
                    <div class="coin-category-card">DEX</div>
                </div>
            </td>
          <td class="lockvalue-col">$10.3B <span class="lockvalue-percent">+14.81%</span> </td>
          <td>23.5%</td>
          <td>23.5%</td>
          <td>23.5%</td>
          <td>23.5%</td>
          <td>23.5%</td>
          <td>23.5%</td>
          <td><LGreenBtn/></td>
      </tr>
  </table>
</template>

<script>
import LGreenBtn from '~/components/Buttons/LGreenBtn.vue'
export default {
    name: 'CompareTableData',
  components: { LGreenBtn },

}
</script>

<style scoped>

    #compare-table 
        td {
           padding: 19px 16px;
        }

</style>