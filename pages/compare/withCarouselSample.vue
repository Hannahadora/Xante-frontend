<template>
  <transition name="carouselSample" class="carouselSample">
      <CompareTable />
  </transition>
</template>

<script>
import CompareTable from '~/components/Tables/CompareTable.vue'
export default {
transition: 'carouselSample',
components: { CompareTable },
}

</script>

<style>
    .carouselSample-enter-active,
    .carouselSample-leave-active {
       transition: all .25s ease-out;
    }
    .carouselSample-enter,
    .carouselSample-leave-to {
        opacity: 0;
        transform-origin: 50% 50%;
    }
</style>