<template>
  <div>
      <h2 class="wrapper ma-headers mb-12 mt-20">Top 10 Liquidity Provisers</h2>
  <table class="top20">
        <tr>
            <th>Name</th>
            <th>Rates</th>
        </tr>
         <tbody>
            <tr>
                <td class="flex items-center lg:gap-3 gap-8">
                    <img class="lg:w-auto w-10 lg:w-auto h-10" src="~/assets/images/Group 30 (3).png" alt="">
                    Provider name</td>
                <td>12%</td>
            </tr>
            <tr>
                <td class="flex items-center lg:gap-3 gap-8">
                    <img class="lg:w-auto w-10 lg:w-auto h-10" src="~/assets/images/Group 30 (4).png" alt="">
                    Provider name</td>
                <td>12%</td>
            </tr>
            <tr>
                <td class="flex items-center lg:gap-3 gap-8">
                <img class="lg:w-auto w-10 lg:w-auto h-10" src="~/assets/images/Group 30 (5).png" alt="">
                Provider name</td>
                <td>13%</td>
            </tr>
            <tr>
                <td class="flex items-center lg:gap-3 gap-8">
                <img class="lg:w-auto w-10 lg:w-auto h-10" src="~/assets/images/Group 30 (3).png" alt="">
                Provider name</td>
                <td>14%</td>
            </tr>
            <tr>
                <td class="flex items-center lg:gap-3 gap-8">
                    <img class="lg:w-auto w-10 lg:w-auto h-10" src="~/assets/images/Group 30 (4).png" alt="">
                    Provider name</td>
                <td>18%</td>
            </tr>
        </tbody>
    </table>
    <div class="w-full mx-auto text-center lg:block hidden" style="background: #0A132B;">
        <button class="font-semi-bold lg:p-9 p-2">Show All</button>
    </div>
</div>
</template>

<script>
export default {
    name: 'Top10'
}
</script>

<style scoped>
    .top10
        td,
        th {
        padding-top: 16px;
        padding-bottom: 16px;
        padding-left: 66px;
    }

    @media screen and (max-width: 768px) {
        td,th {
            padding-top: 28px !important;
            padding-bottom: 28px !important;
            padding-left: 25px !important;
            font-size: 12px;
        }
    }
</style>