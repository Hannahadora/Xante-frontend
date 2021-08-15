<template>
  <div class="">
    <h2 class="ma-headers mt-40 wrapper">Market Analytics</h2>

      <div class="mt-12 lg:flex block items-center justify-between wrapper">
        <div class="flex items-start">
          <div
            class="lg:h-14 h-10 flex lg:items-center items-start gap-2 lg:mr-4"
            style="background: #1f2b4a"
          >
            <p class="lsca active md:m-1">Locked Value</p>
            <p class="lsca">Stable coin Analysis</p>
            <plus-icon class="m-1" />
          </div>
          <!-- <ProviderDropdown /> -->
        </div>

        <div class="lg:flex hidden items-center gap-2">
          <tab class="active-tab">ALL</tab>
          <tab>DEFI</tab>
          <tab>NFT</tab>
          <tab>HECO</tab>
        </div>
      </div>

      <div class="wrapper lg:mt-10 mt-20 mb-4 flex items-end lg:justify-start justify-end lg:gap-12">
        <div>
          <div class="flex items-center gap-2">
            <Color theme="yellow" />
            <h5 class="inter lg:text-2xl text-xs">$92.88B</h5>
          </div>
          <span class="small-text ml-4 lg:text-sm font-light">Gross value locked</span>
        </div>
        <div>
          <div class="flex items-center gap-2">
            <Color theme="green" />
            <h5 class="inter lg:text-2xl text-xs">$92.88B</h5>
          </div>
          <span class="small-text ml-4 lg:text-sm font-light">Net value locked</span>
        </div>
      </div>

    <div class="wrapper">
      <graph></graph>

      <table class="w-full mb-6 lg:table hidden">
        <tr>
          <th>Name</th>
          <th>Chain</th>
          <th>Category</th>
          <th>Locked value</th>
        </tr>

      <tbody>
        <tr
          class=""
          v-for="ma in marketAnalytics"
          :key="ma"
        >
          <td class="flex items-center gap-3">
            <img :src="ma.img" alt="" />
            {{ ma.name }}
          </td>
          <td>{{ ma.chain }}</td>
          <td>
            <div class="coin_category-grid">
              <div
                class="coin-category"
                v-for="category in ma.category"
                :key="category"
              >
                {{ category }}
              </div>
            </div>
          </td>
          <td>{{ ma.locked_value }}</td>
        </tr>

        <tr
          class=""
          v-for="ma in marketAnalytics"
          :key="ma"
        >
          <td class="flex items-center gap-3">
            <img :src="ma.img" alt="" />
            {{ ma.name }}
          </td>
          <td>{{ ma.chain }}</td>
          <td>
            <div class="coin_category-grid">
              <div
                class="coin-category"
                v-for="category in ma.category"
                :key="category"
              >
                {{ category }}
              </div>
            </div>
          </td>
          <td>{{ ma.locked_value }}</td>
        </tr>

        <tr
          class=""
          v-for="ma in marketAnalytics"
          :key="ma"
        >
          <td class="flex items-center gap-3">
            <img :src="ma.img" alt="" />
            {{ ma.name }}
          </td>
          <td>{{ ma.chain }}</td>
          <td>
            <div class="coin_category-grid">
              <div
                class="coin-category"
                v-for="category in ma.category"
                :key="category"
              >
                {{ category }}
              </div>
            </div>
          </td>
          <td>{{ ma.locked_value }}</td>
        </tr>

        <tr
          class=""
          v-for="ma in marketAnalytics"
          :key="ma"
        >
          <td class="flex items-center gap-3">
            <img :src="ma.img" alt="" />
            {{ ma.name }}
          </td>
          <td>{{ ma.chain }}</td>
          <td>
            <div class="coin_category-grid">
              <div
                class="coin-category"
                v-for="category in ma.category"
                :key="category"
              >
                {{ category }}
              </div>
            </div>
          </td>
          <td>{{ ma.locked_value }}</td>
        </tr>

        <tr
          class=""
          v-for="ma in marketAnalytics"
          :key="ma"
        >
          <td class="flex items-center gap-3">
            <img :src="ma.img" alt="" />
            {{ ma.name }}
          </td>
          <td>{{ ma.chain }}</td>
          <td>
            <div class="coin_category-grid">
              <div
                class="coin-category"
                v-for="category in ma.category"
                :key="category"
              >
                {{ category }}
              </div>
            </div>
          </td>
          <td>{{ ma.locked_value }}</td>
        </tr>

        <tr
          class=""
          v-for="ma in marketAnalytics"
          :key="ma"
        >
          <td class="flex items-center gap-3">
            <img :src="ma.img" alt="" />
            {{ ma.name }}
          </td>
          <td>{{ ma.chain }}</td>
          <td>
            <div class="coin_category-grid">
              <div
                class="coin-category"
                v-for="category in ma.category"
                :key="category"
              >
                {{ category }}
              </div>
            </div>
          </td>
          <td>{{ ma.locked_value }}</td>
        </tr>

        </tbody>
      </table>
    </div>

    <!-- *****************MOBILe -->

    <div class="my-11">
      <div class="mobile-a-table lg:hidden block" v-for="ma in marketAnalytics" :key="ma">
          <div class="flex items-center gap-3 mb-5">
              <img :src="ma.img" alt=""  class="w-10 h-10"/>
              {{ ma.name }}
            </div>

           <div class="flex items-center justify-between mb-4">
               <span>Chain</span>
               <span>{{ ma.chain }}</span>
           </div>

           <div class="flex items-center justify-between mb-4">
               <span>Category</span>
               <span>{{ ma.category }}</span>
           </div>

           <div class="flex items-center justify-between">
               <span>Locked Value</span>
               <span>{{ ma.locked_value }}</span>
           </div>
      </div>
    </div>
  </div>
</template>

<script>
import Color from "~/components/Color.vue";
import Graph from "~/components/Graph.vue";
import Tab from "~/components/Tab.vue";

export default {
  name: "analytics",
  components: { Color, Graph, Tab },
  data() {
    return {};
  },

  computed: {
    marketAnalytics() {
      return this.$store.state.marketAnalytics;
    },
  },
};
</script>

<style scoped>

  table {
    margin-top: 2px;
  }

  td, th {
    padding: 16px 75px;
  }

  .mobile-a-table {
    background: #0A132A;
    margin-top: 4px;
    padding: 16px 24px 29px 24px;
  }

  .active {
    background: #056237;
    border-radius: 4px;
  }

  .lsca {
    padding: 12px 20px;
  }

  @media screen and (max-width: 768px) {
    h5 {
      font-size: 12px  !important;
    }

    .small-text {
      font-size: 9px;
    }

    p {
      font-size: 12px;
    }
  }

   @media screen and (max-width: 280px) {
     p {
       font-size: 10px;
     }

     h5 {
      font-size: 10px  !important;
    }

    .small-text {
      font-size: 7px;
    }
    .active {
      background: #281E5D;
    }

    .lsca {
      padding: 11px 13.5px;
    }
   }
</style>