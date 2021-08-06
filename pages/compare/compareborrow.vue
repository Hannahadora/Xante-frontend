<template>
  <transition name="compareborrow" class="compare-borrow">
      <CompareTable />
  </transition>
</template>

<script>
import CompareTable from '~/components/Tables/CompareTable.vue'
export default {
  components: { CompareTable },
    name: 'compareborrow',
    transition: 'compareborrow'
}
</script>

<style scoped>
    .compareborrow-enter-active,
    .compareborrow-leave-active {
        transition: all .25s ease-out;
    }
    .compareborrow-enter,
    .compareborrow-leave-to {
        opacity: 0;
        transform-origin: 50% 50%;
    }
</style>