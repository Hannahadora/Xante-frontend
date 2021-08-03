<template>
    <div>
        <table id="coin_table" class="mt-4 w-full">
            <tr>
                <th>Platform</th>
                <th>Category</th>
                <th>Locked Value</th>
                <th>Borrow APY</th>
                <th>Lend APY</th>
                <th>Borrow APY</th>
                <th></th>
            </tr>

            <tr class="border-b border-gray-700">
                <td>
                    <img src="~/assets/images/Aave.png" alt="">
                    Aave</td>
                <td class="coin_category-grid">
                    <div class="coin-category-card">DEX</div>
                    <div class="coin-category-card">AMM</div>
                    <div class="coin-category-card col-span-2">Synthetic Assets</div>
                </td>
                <td>$10.30</td>
                <td>$23.5%</td>
                <td>$23.5%</td>
                <td>$23.5%</td>
                <td><LGreenBtn /></td>
            </tr>

            <tr class="border-b border-gray-700">
                <td>
                    <img src="~/assets/images/Binance.png" alt="">
                    Binance</td>
                <td class="coin_category-grid">
                    <div class="coin-category-card">DEX</div>
                </td>
                <td>$10.30</td>
                <td>$23.5%</td>
                <td>$23.5%</td>
                <td>$23.5%</td>
                <td><LGreenBtn /></td>
            </tr>

             <tr class="border-b border-gray-700">
                <td>
                    <img src="~/assets/images/Compound.png" alt="">
                    Compound</td>
                <td class="coin_category-grid">
                    <div class="coin-category-card">DEX</div>
                    <div class="coin-category-card">DEX</div>
                </td>
                <td>$10.30</td>
                <td>$23.5%</td>
                <td>$23.5%</td>
                <td>$23.5%</td>
                <td><LGreenBtn /></td>
            </tr>


             <tr class="border-b border-gray-700">
                <td>
                    <img src="~/assets/images/Binance.png" alt="">
                    Binance</td>
                <td class="coin_category-grid">
                    <div class="coin-category-card">DEX</div>
                    <div class="coin-category-card">AMM</div>
                    <div class="coin-category-card col-span-2">Synthetic Assets</div>
                </td>
                <td>$10.30</td>
                <td>$23.5%</td>
                <td>$23.5%</td>
                <td>$23.5%</td>
                <td><LGreenBtn /></td>
            </tr>

            <tr class="border-b border-gray-700">
                <td>
                    <img src="~/assets/images/Aave.png" alt="">
                    Aave</td>
                <td class="coin_category-grid">
                    <div class="coin-category-card">DEX</div>
                </td>
                <td>$10.30</td>
                <td>$23.5%</td>
                <td>$23.5%</td>
                <td>$23.5%</td>
                <td><LGreenBtn /></td>
            </tr>

        </table>

         <div class="w-full mx-auto text-center" style="background: #0A132B;">
            <button class="font-semi-bold p-9">Show All</button>
        </div>
    </div>
</template>

<script>

import LGreenBtn from './Buttons/LGreenBtn.vue'

export default {
  components: { LGreenBtn },
    name: 'Coins'

}
</script>

<style scoped>

td,
th {
    padding-left: 46px;
    padding-top:18px;
    padding-bottom: 18px;
}

</style>