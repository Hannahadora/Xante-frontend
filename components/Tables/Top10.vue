<template>
  <div>
      <h2 class="ma-headers mb-12 mt-20">Top 10 Liquidity Provisers</h2>
      <table class="top10">
        <tr>
            <th>Name</th>
            <th>Rates</th>
        </tr>
        <tbody>
            <tr>
                <td class="flex items-center gap-3">
                    <img src="~/assets/images/Group 30 (3).png" alt="">
                    Provider name</td>
                <td>12%</td>
            </tr>
            <tr>
                <td class="flex items-center gap-3">
                    <img src="~/assets/images/Group 30 (4).png" alt="">
                    Provider name</td>
                <td>12%</td>
            </tr>
            <tr>
                <td class="flex items-center gap-3">
                <img src="~/assets/images/Group 30 (5).png" alt="">
                Provider name</td>
                <td>13%</td>
            </tr>
            <tr>
                <td class="flex items-center gap-3">
                <img src="~/assets/images/Group 30 (3).png" alt="">
                Provider name</td>
                <td>14%</td>
            </tr>
            <tr>
                <td class="flex items-center gap-3">
                    <img src="~/assets/images/Group 30 (4).png" alt="">
                    Provider name</td>
                <td>18%</td>
            </tr>
        </tbody>
    </table>
        <div class="w-full mx-auto text-center" style="background: #0A132B;">
        <button class="font-semi-bold p-9">Show All</button>
    </div>
</div>
</template>

<script>
export default {
    name: 'Top10'
}
</script>

<style>
    .top10
        td,
        th {
        padding-top: 16px;
        padding-bottom: 16px;
        padding-left: 66px;
    }
</style>