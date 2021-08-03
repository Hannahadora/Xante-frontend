<template>
  <div id="opport">
      <Header />

      <div id="opport-view" class="">
        <h2 class="font-semi-bold sharp-sans md:ml-0 ml-6">Opportunities</h2>

        <div class="md:mt-36 mt-8 strategy-sect">
          <div class="strategy-text" style="">
            <span class="md:text-2xl text-lg md:mb-8 mb-6">DEFI Stategy</span>
            <p class="mt-8">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
            <p class="lg:block hidden">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
          </div>
          <div class="opport-box"></div>   
        </div>

        <div class="md:mt-16 mt-10 strategy-sect2">
          <div class="opport-box"></div>   
          <div class="strategy-text" style="">
            <span class="md:text-2xl text-lg md:mb-8 mb-6">CEFI Stategy</span>
            <p class="mt-8">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
            <p class="lg:block hidden">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
          </div>   
        </div>

        <div class="md:mt-16 mt-10 strategy-sect">     
          <div class="strategy-text" style="">
            <span class="md:text-2xl text-lg md:mb-8 mb-6">Shaking Stategy</span>
            <p class="md:mt-8 mt-6">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
            <p class="lg:block hidden">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
          </div>
          <div class="opport-box"></div>   
        </div>

        <div class="md:mt-16 mt-10 strategy-sect2">
           <div class="opport-box"></div>   
            <div class="strategy-text" style="">
              <span class="md:text-2xl text-lg md:mb-8 mb-6">Farming Stategy</span>
              <p class="md:mt-8 mt-6">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
              <p class="lg:block hidden">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
            </div>      
        </div>

        <div class="md:mt-16 mt-10 strategy-sect">     
          <div class="strategy-text" style="">
            <span class="md:text-2xl text-lg md:mb-8 mb-6">Exponential Growth Stategy</span>
            <p class="md:mt-8 mt-6">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
            <p class="lg:block hidden">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
          </div>  
          <div class="opport-box"></div>       
        </div>

        <div class="md:mt-16 mt-10 strategy-sect2">
           <div class="opport-box"></div>   
            <div class="strategy-text" style="">
              <span class="md:text-2xl text-lg md:mb-8 mb-6">DEFI Stategy</span>
              <p class="">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
              <p class="lg:block hidden">Xante will connect to Lenders, Partners, and Credit Providers via API, aggregating their product attributes and lending criteria in order to present consumers with offers in real time</p>
            </div>      
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
    padding: 150px 120px 332px 120px;
}

.opport-box {
    height: 518px;
    width: 687px;
    background: #0A1227;
}

.strategy-text {
  width: 378px;
  /* margin-right: 126px; */
}

.strategy-sect {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  gap: 126px;
}

.strategy-sect2 {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  gap: 126px;
}

@media screen and (max-width: 768px) {
  #opport-view {
    padding: 110px 24px 329px 24px;
  }
}

@media screen and (max-width: 500px) {
  #opport-view {
    padding: 110px 0px 329px 0px;
  }

  .strategy-sect {
    flex-direction: column;
  }

  .strategy-sect2 {
    flex-direction: column-reverse;
  }

  .strategy-text {
    padding: 43px 56px 16px 24px;
    /* width: 295px; */
  }

  .opport-box {
    height: 312px;
    width: 100%;
}
}
</style>