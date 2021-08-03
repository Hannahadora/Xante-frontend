<template>
  <div>
      <table class="cat-n-val w-full">
        <tr>
            <th>Name</th>
            <th>Chain</th>
            <th>Category</th>
            <th>Locked value</th>
        </tr>

        <tr class="border-b border-gray-700">
            <td class="flex items-center gap-3">
                <img src="../assets/images/Group 30 (3).png" alt="">
                Provider name</td>
            <td>Bsc</td>
            <td>
                <div class="coin_category-grid">
                    <div class="coin-category-card">DEX</div>
                </div>
            </td>
            <td>$15.0 B</td>
        </tr>

        <tr class="border-b border-gray-700">
            <td class="flex items-center gap-3">
                <img src="../assets/images/Group 30 (4).png" alt="">
                Provider name</td>
            <td>Bsc</td>
            <td>
                <div class="coin_category-grid">
                    <div class="coin-category-card">DEX</div>
                    <div class="coin-category-card">DEX</div>
                </div>
            </td>
            <td>$15.0 B</td>
        </tr>

        <tr>
            <td class="flex items-center gap-3">
                <img src="../assets/images/Group 30 (5).png" alt="">
                Provider name</td>
            <td>Bsc</td>
            <td>
                <div class="coin_category-grid">
                    <div class="coin-category-card">DEX</div>
                    <div class="coin-category-card">DEX</div>
                </div>
            </td>
            <td>$15.0 B</td>
        </tr>
    </table> 
  </div>
</template>

<script>
export default {
    name: 'CategValue'
}
</script>

<style>
    .cat-n-val
        th,
        td {
            padding-left: 66px;
            padding-top: 16px;
            padding-bottom: 16px;
        }

</style>