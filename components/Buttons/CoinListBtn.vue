<template>
  <button id="coinlist-btn" :class="{ active: theme === 'active' }">
      {{ text }}
  </button>
</template>

<script>
export default {
    name: 'coinlistbtn',
    props: ['text', 'theme']

}
</script>

<style scoped>
 #coinlist-btn {
    width: 71px;
    height: 56px;
    padding: 12px;
    text-align: center;
    background: #1F2B4A !important;
    border-radius: 4px;
 }

 #coinlist-btn.active {
    background: #281E5D !important;
 }

</style>