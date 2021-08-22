<template>
  <div class="metric-view">
    <div class="wrapper">
      <h2 class="ma-headers mb-7">Compare Coins</h2>
      <span class="text-sm mb-4">Type in coin to compare</span>
    </div>

      <div class="table-div">
        <table class="metric-table">
        <tr>
          <th></th>
          <th>
            <div class="lg:flex flex-col items-center justify-center lg:gap-9">
            <img class="lg:w-auto w-5" src="./images/Group 30 (2).png" alt="">
           <span class="lg:block hidden">Bitcoin</span></div>
          </th>
          <th>
            <div class="lg:flex flex-col items-center justify-center lg:gap-9">
            <img class="lg:w-auto w-5" src="./images/Group 30.png" alt="">
            <span class="lg:block hidden">Ethereum</span></div>
          </th>
        </tr>
       <tbody>
        <tr v-for="(param, a) in params" :key="a">
          <td>
            {{ param.name }}
          </td>
          <td>{{ param.value }}</td>
          <td>{{ param.value }}</td>
        </tr>
       </tbody>
      </table>
      </div>
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
      return this.$store.state.params
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
  .table-div {
    margin: 80px 120px;
  }

    @media screen and (max-width: 540px) {
      td, th {
        padding: 20px !important;
      }
      .table-div {
        margin: 80px 0px !important;
      }
    }
</style>
