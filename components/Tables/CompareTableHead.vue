<template>
  <table>
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
  </table>
</template>

<script>
export default {
    name: 'CompareTableHead'
}
</script>

<style scoped>
    th {
      padding: 19px 20px;
      /* text-align: left; */
      vertical-align: bottom;
    }

    tr {
      border-bottom: 1px solid #151F38;
    }
</style>