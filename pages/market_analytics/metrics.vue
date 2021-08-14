<template>
  <div class="metric-view wrapper">
    <h2 class="ma-headers mb-7">Compare Coins</h2>
    <span class="text-sm mb-4">Type in coin to compare</span>
      <table class="metric-table mt-20">
        <tr>
          <th></th>
          <th>BitCoin</th>
          <th>Ethereum</th>
        </tr>
       <tbody>
        <tr v-for="param in params" :key="param">
          <td>
            {{ param.name }}
          </td>
          <td>{{ param.value }}</td>
          <td>{{ param.value }}</td>
        </tr>
       </tbody>
      </table>
  </div>
</template>

<script>
export default {
  name: 'metrics',

  data() {
    return {
      // param: '',
      metrics: ''
    }
  },

  mounted() {
     this.metrics = this.$store.state.metrics;
  },

  computed: {
    params() {
      return this.$store.getters.params
    }
  }
}
</script>

<style scoped>
  .metric-view {
    margin-top: 154px;
    margin-bottom: 82px;
  }
  td {
       padding-left: 107px;
    }
</style>