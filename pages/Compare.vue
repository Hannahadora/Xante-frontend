<template>
  <div>
      <Header />
      <div class="compare-view">
        <h2 class="sharp-sans font-bold" style="width: 687px">Compare Centralised and Decentralised Cryptocurrency Financial Markets.</h2>
        <p class="mt-2 md:block hidden">Compare the best lend and borrow rate for your <br>
            crypto assets across Defi protocols and Providers.</p>

        <div class="lg:flex block items-center justify-between">
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

          <div class="linknsearch-grid">
            <div class="cls lg:mb-6">
              <NuxtLink to="/compare/" class="cl md:px-7 px-3 md:py-2 py-1  rounded-3xl">Lending</NuxtLink>
              <NuxtLink to="/compare/compareborrow" class="cl md:px-7 px-3 md:py-2 py-1 rounded-3xl">Borrowing</NuxtLink>
            </div>

            <form class="search-box md:mr-0 mr-4">
              <div class="flex items-center">
                <img class="md:mr-3 mr-2 w-3 h-3" src="assets/images/search.png" alt="">
                <input type="text" class="bg-transparent focus:outline-none md:text-sm text-xs" placeholder="Search Coin">
              </div>
              <img src="assets/images/shape.png" alt="">
            </form>
          </div>

        </div>
      </div>

      <div class="xl:mx-10 mx-0 mb-40">

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
    grid-template-columns: 50% 50% 50%;
    gap: 8px;
  }
  .compare-filter-option {
    padding: 4px 8px;
    background: #1F2B4A;
    border-radius: 2px;
    max-width: 118px;
    cursor: pointer;
  }

  .cls {
    background: #0A1227;
    border-radius: 24px;
    display: flex;
    align-items: center;
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

.linknsearch-grid {
  display: grid;
  flex-direction: row;
  justify-items: end;
}






  @media screen and (max-width: 768px) {
     .linknsearch-grid {
      display: grid;
      flex-direction: flex;
      grid-template-columns: 50% 50%;
      align-items: end;
      justify-items: baseline;
      margin-bottom: 44px;
    }

      .compare-filters {
        width: 30%;
    }

  }

  @media screen and (max-width: 1024px) {
     .compare-filters {
        width: 30%;
    }

    .compare-view {
      margin: 160px 24px 0 24px;
    }

    .cls {
      width: 250px;
    }

  }

  @media screen and (max-width: 540px) {
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
      width: 100%;
      height: 39px;
      padding: 12px 13px;
      order: 1;
    }

    .cl {
      font-size: 12px !important;
    }

    .linknsearch-grid {
      display: grid;
      flex-direction: column;
      grid-template-columns: 50% 50%;
      align-items: end;
      justify-content: space-between;
    }

    .linknsearch-grid :nth-child(2) {
      order: 1;
    }

    .cls {
      width: 150px;
      height: fit-content !important;
    }
  }




</style>
