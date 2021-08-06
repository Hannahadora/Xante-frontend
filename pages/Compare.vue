<template>
  <div>
      <Header />
      <div class="compare-view">
        <h2 class="sharp-sans font-bold" style="width: 687px">Compare Centralised and Decentralised Cryptocurrency Financial Markets.</h2>
        <p class="mt-2">Compare the best lend and borrow rate for your <br>
            crypto assets across Defi protocols and Providers.</p>

        <div class="flex items-center justify-between">
          <div class="compare-filters mt-10 mb-16">
          <p class="compare-filter-option active-filter col-span-3">All Markets</p>
          <p class="compare-filter-option">Centralized</p>
          <p class="compare-filter-option col-span-2">Decentralized</p>
          <p class="compare-filter-option">Stable coins</p>
          <select class="compare-filter-option" name="categories" id="">
            <option value="0">Categories</option>
          </select>
          <select class="compare-filter-option" name="titleList" id="">
            <option value="0">Title list</option>
          </select>
        </div>

        <div>
          <div class="flex items-center mb-6" style="background: #0A1227; border-radius: 24px; width: 240px">
            <p class="px-7 py-2 active-filter rounded-3xl">Lending</p>
            <p class="px-7 py-2 rounded-3xl">Borrowing</p>
          </div>
        </div>

        </div>
      </div>
      
      <CompareTable  class="mx-10 mb-16"/>
      <Footer />
  </div>
</template>

<script>
import Footer from '~/components/Footer.vue'
import Header from '~/components/Header.vue'
import CompareTable from '~/components/Tables/CompareTable.vue'
import CompareTableHead from '~/components/Tables/CompareTableHead.vue'
export default {
    name: 'Compare',
    components: { Footer, Header, CompareTable, CompareTableHead,}
}
</script>

<style>
  .compare-view {
    margin:160px 120px 0px 120px;
  }
</style>