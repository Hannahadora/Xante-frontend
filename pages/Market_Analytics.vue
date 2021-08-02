<template>
  <div>
      <Header />
        <div id="market-view">
            <h2 class="inter">Market Analytics</h2>
            <span class="mt-7 mb-4">Type in coin to compare</span>

            <div class="marketCoinPrice-sect">
                <h2 class="inter font-medium">Coin Price</h2>

                <table class="mt-4 w-full">
                    <tr>
                        <th>Name</th>
                        <th>Price</th>
                        <th>Market Cap</th>
                        <th>Last 7d</th>
                    </tr>

                    <tr>
                        <td>Tether</td>
                        <td>Bsc</td>
                        <td>$15.0 B</td>
                        <td>$15.0 B</td>
                    </tr>

                    <tr>
                        <td>USD Coin</td>
                        <td>Bsc</td>
                        <td>$15.0 B</td>
                        <td>$15.0 B</td>
                    </tr>

                    <tr>
                        <td>Binance USD</td>
                        <td>Bsc</td>
                        <td>$15.0 B</td>
                        <td>$15.0 B</td>
                    </tr>
                </table>
            </div>

            <div class="rect_14 mt-24">
                <div class="bg_11">
                    <img src="../assets/images/Group 11.png" alt="">
                </div>
                <div>
                    <p>Get access to<br>
                    deeper market insight<br>
                    when you join us</p>
                    <DGreenBtn class="mt-6" text="Join Now" />
                </div>
            </div>
        </div>
      <Footer />
  </div>
</template>

<script>
import DGreenBtn from '~/components/Buttons/DGreenBtn.vue'
import Footer from '~/components/Footer.vue'
import Header from '~/components/Header.vue'
export default {
  components: { Header, Footer, DGreenBtn },
    name: 'MarketAnalytics'

}
</script>

<style>
    #market-view {
        padding: 81px 120px 130px 120px;
    }

    .bg_11 {
        height: 273px;
        width: 326px;
        border-radius: 10px;
        background: #151F38;
        padding: 27px 30px;
        margin-right: 345px;
    }

    .rect_14 {
        width: 100%;
        height: 352px;
        padding: 39px 66px;
        background: #0A132B;
        display: flex;
        align-items: center;
    }

</style>