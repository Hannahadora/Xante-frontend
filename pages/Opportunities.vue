<template>
  <div id="opport">
      <Header />

      <div id="opport-view" class="">
        <h2 class="font-semi-bold sharp-sans">Opportunities</h2>
        <div class="mt-36 flex items-start justify-between">
            <div class="" style="width: 378px">
              <span class="text-2xl mb-8">DEFI Stategy</span>
              <p class="mt-8">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
              <p>Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
            </div>
            <div class="opport-box"></div>   
        </div>
      </div>
        
      <Footer />
  </div>
</template>

<script>
import Footer from '~/components/Footer.vue'
import Header from '~/components/Header.vue'
export default {
  components: { Header, Footer },
    name: 'Opportunities',

}
</script>

<style>
#opport {
    background: #151F38;
}

#opport-view {
    padding: 107px 120px;
}

.opport-box {
    height: 518px;
    width: 687px;
    background: #0A1227;
}
</style>