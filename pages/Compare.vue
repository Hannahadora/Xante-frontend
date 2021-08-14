<template>
  <div>
      <Header />
      <div class="compare-view">
        <h2 class="sharp-sans font-bold" style="width: 687px">Compare Centralised and Decentralised Cryptocurrency Financial Markets.</h2>
        <p class="mt-2 md:block hidden">Compare the best lend and borrow rate for your <br>
            crypto assets across Defi protocols and Providers.</p>

        <div class="md:flex block items-center justify-between">
          <div class="compare-filters grid-cols-3 mt-10 mb-16">
          <p class="compare-filter-option active-filter md:col-span-3">All Markets</p>
          <p class="compare-filter-option">Centralized</p>
          <p class="compare-filter-option md:col-span-2">Decentralized</p>
          <p class="compare-filter-option">Stable coins</p>
          <select class="compare-filter-option" name="categories" id="">
            <option value="0">Categories</option>
          </select>
          <select class="compare-filter-option" name="titleList" id="">
            <option value="0">Title list</option>
          </select>
        </div>

        <div class="flex md:flex-col flex-row items-end">
          <div class="flex items-center mb-6" style="background: #0A1227; border-radius: 24px;">
            <NuxtLink to="/compare/" class="cl px-7 py-2  rounded-3xl">Lending</NuxtLink>
            <NuxtLink to="/compare/compareborrow" class="cl p-7 py-2 rounded-3xl">Borrowing</NuxtLink>
          </div>

          <form class="search-box">
            <div class="flex items-center">
              <img class="mr-3" src="~/assets/images/search.png" alt="">
              <input type="text" class="bg-transparent focus:outline-none text-sm" placeholder="Search Coin">
            </div>
            <img src="~/assets/images/shape.png" alt="">
          </form>
        </div>

        </div>
      </div>

      <div class="md:mx-10 mx-0 mb-40">

         <NuxtChild  />
  
      </div>
      
      <Footer />
  </div>
</template>

<script>
import Footer from '~/components/Footer.vue'
import Header from '~/components/Header.vue'
export default {
    name: 'compare',
    components: { Footer, Header, }
}
</script>

<style scoped>
  .compare-view {
    margin:160px 120px 0px 120px;
  }

  .compare-filters {
    width: 20%;
    display: grid;
    /* grid-template-columns: 50% 50% 50%; */
    gap: 8px;
  }
  .compare-filter-option {
    padding: 4px 8px;
    background: #1F2B4A;
    border-radius: 2px;
    max-width: 118px;
    cursor: pointer;
  }

  a.nuxt-link-exact-active {
    background-color: #056237;
  }

  .search-box {
    width: 377px;
    height: 52px;
    background: #0A1227;
    border-radius: 4px;
    padding: 18.5px 22.67px 18.5px 18.5px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

  @media screen and (max-width: 400px) {
    .compare-view {
      margin: 100px 24px;
    }

    h2 {
      font-size: 18px !important;
      line-height: 29.27px;
      width: 319px !important;
    }

    .compare-filters {
      width: 100%;
     	grid-template-columns: repeat(3, minmax(0, 1fr));
    }

    .search-box {
      width: 156px;
      height: 39px;
    }

    .cl {
      padding: 5px 18px;
      font-size: 12px !important;
    }
  }




</style>