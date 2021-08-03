<template>
  <div>
      <Header />
        <div id="market-view">
            <h2 class="inter mt-20">Market Analytics</h2>
            <span class="mt-7 mb-4">Type in coin to compare</span>

            
            <div class="mt-14 flex items-center justify-between">
                <div class="flex items-center">
                    <div class="h-14 flex items-center gap-2 mr-4" style="background: #1F2B4A;">
                        <p class="py-3 px-5 m-1 rounded" style="background:#056237;">Locked Value</p>
                        <p class="py-3 px-5">Stable coin Analysis</p>
                       <plus-icon class="m-1"/>
                    </div>
                    <select name="" id="" class="py-4 px-5 rounded" style="background: #1F2B4A;">
                        <option value="" selected>Top 10 Providers</option>
                    </select>
                </div>

                <div class="flex items-center gap-2">
                    <CoinListBtn text="ALL" theme="active" />
                    <CoinListBtn text="DEFI" />
                    <CoinListBtn text="NFT" />
                    <CoinListBtn text="HECO" />
                </div>
            </div>

            <div class="mt-12 flex items-center gap-12">
                <div>
                    <div class="flex items-center gap-2">
                        <Color theme="yellow" />
                        <span class="i gap-2 text-2xl">$92.88B</span>
                    </div>
                    <span class="ml-4 text-sm font-light">Gross value locked</span>
                </div>
                <div>
                    <div class="flex items-center gap-2">
                        <Color theme="green" />
                        <span class="inter text-2xl">$92.88B</span>
                    </div>
                    <span class="ml-4 text-sm font-light">Net value locked</span>
                </div>
            </div>




            <graph></graph>
     
            <CategValue class="mt-1"/>
            
            <h2 class="inter mb-14 mt-44">Stable Coin Analysis</h2>
            <div class="w-full mb-6 flex items-end justify-between">
                <div class="flex items-end gap-2">
                    <CoinListBtn text="USDT" theme="active" />
                    <CoinListBtn text="USDC" />
                    <CoinListBtn text="BUSD" />
                    <ArrowBtn />
                    <span class="text-xs">More coins</span>
                </div>
                <div class="">
                    <span class="text-sm font-light mr-3">USDT</span>
                    <span class="text-2xl font-medium">$1.00</span>
                </div>
            </div>
                 
            <graph>
                
            </graph>
        
            <LendBorrow class="mt-1"/>

            <div id="ma_tops">
                <div class="w-1/2">
                    <h2 class="inter mb-12 mt-20">Top 10 Liquidity Provisers</h2>
                    <Top10 />
                </div>

                <div class="w-1/2">
                    <h2 class="inter mb-12 mt-20">Top 20 Borrow Rates</h2>
                    <Top-20 />
                </div>
            </div>



            <h2 class="font-medium inter mb-12 mt-28">Compare coins</h2>
                <table id="ma_table06" class="mb-24">
                    <tr>
                        <td rowspan="2" class="inter text-2xl">Compare coins different <br>
                            coins using varieties of <br>
                            metrics</td>
                        <td><img class="w-12 h-12" src="../assets/images/Group 30 (1).png" alt=""></td>
                        <td><img class="w-12 h-12" src="../assets/images/Group 30.png" alt=""></td>
                    </tr>
                    <tr>
                        <td>Bitcoin</td>
                        <td>Ethereum</td>
                    </tr>
                    <tr>
                        <td><DGreenBtn text="Compare" /></td>
                        <td>$15.0.B</td>
                        <td>$15.0.B</td>
                    </tr>
                </table>


                <Coins />
        

            <div class="marketCoinPrice-sect mt-28">
                <h2 class="inter font-medium">Coin Price</h2>

                <p class="px-4 py-4 my-7 w-24 rounded" style="background: #281E5D;">BTC</p>
                <MarketCap />
                 <div class="w-full mx-auto text-center" style="background: #0A132B;">
                    <button class="font-semi-bold p-9">Show All</button>
                </div>     
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
import ArrowBtn from '~/components/Buttons/ArrowBtn.vue'
import CoinListBtn from '~/components/Buttons/CoinListBtn.vue'
import DGreenBtn from '~/components/Buttons/DGreenBtn.vue'
import CategValue from '~/components/CategValue.vue'
import Coins from '~/components/Coins.vue'
import Color from '~/components/Color.vue'
import Footer from '~/components/Footer.vue'
import Graph from '~/components/Graph.vue'
import Header from '~/components/Header.vue'
import LendBorrow from '~/components/LendBorrow.vue'
import MarketCap from '~/components/MarketCap.vue'
import Top10 from '~/components/Top10.vue'
import Top20 from '~/components/Top20.vue'
export default {
  components: { Header, Footer, DGreenBtn, Coins, CoinListBtn, ArrowBtn, Color, Graph, Top10, Top20, CategValue, LendBorrow, MarketCap },
  name: 'MarketAnalytics'

}
</script>

<style scoped>
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

    #ma_table06 td {
       padding-left: 107px;
    }

    #ma_tops {
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: start;
        gap: 32px;
    }

    #ma_table05 
        td,
        th {
        padding-top: 16px;
        padding-bottom: 16px;
        padding-left: 66px;
    }

</style>