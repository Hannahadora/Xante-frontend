<template>
   <transition name="compare-lend" class="compare-lend">
      <CompareTable />
  </transition>
</template>

<script>
import CompareTable from '~/components/Tables/CompareTable.vue'
export default {
  transition: 'compare-lend',
  components: { CompareTable },
}
</script>

<style>
    .compare-lend-enter-active,
    .compare-lend-leave-active {
        transition: all .25s ease-out;
    }
    .compare-lend-enter,
    .compare-lend-leave-to {
        opacity: 0;
        transform-origin: 50% 50%;
    }
</style>