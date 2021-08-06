<template>
  <table id="compare-table">
     <CompareTableHead />
     <CompareTableData />
     <CompareTableData />
     <CompareTableData />
     <CompareTableData />
     <CompareTableData />
  </table>
</template>

<script>
import LGreenBtn from '~/components/Buttons/LGreenBtn.vue'
import CompareTableData from './CompareTableData.vue'
import CompareTableHead from './CompareTableHead.vue'
export default {
    name: 'CompareTable',
  components: { LGreenBtn, CompareTableData, CompareTableHead },

}
</script>

<style scoped>

    #compare-table 
        td {
           padding: 19px 16px;
        }

</style>