<template>
  <div class="wrapper ">
    <div class="mt-20 flex items-center justify-between">
      <div class="flex items-start">
        <div
          class="h-14 flex items-center gap-2 mr-4"
          style="background: #1f2b4a"
        >
          <p class="py-3 px-5 m-1 rounded" style="background: #056237">
            Locked Value
          </p>
          <p class="py-3 px-5">Stable coin Analysis</p>
          <plus-icon class="m-1" />
        </div>
        <!-- <ProviderDropdown /> -->
      </div>

      <div class="mt-12 flex items-center gap-12">
        <div>
          <div class="flex items-center gap-2">
            <Color theme="yellow" />
            <span class="inter text-2xl">$92.88B</span>
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
    </div>

    <div class="flex items-center gap-2 mb-20">
      <tab class="active-tab">ALL</tab>
      <tab>DEFI</tab>
      <tab>NFT</tab>
      <tab>HECO</tab>
    </div>

    <graph></graph>

    <table class="cat-n-val w-full mb-6">
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
</style>