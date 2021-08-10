<template>
  <div class="provider-dropdown relative">
    <div class="py-4 px-5 rounded p-dropdown" style="">
      <span>Top 10 Providers</span> <img src="../assets/images/ic-arrowdown.png" alt="" />
    </div>
    <div v-if="openPDropdown" class="p-dropdown-content text-white p-2">
      <p class="e-dv">Top 10 Borrow Rates</p>
      <p class="e-dv">Top 10 Provider</p>
      <p class="e-dv">Compare Provider</p>
      <p class="e-dv">Coin Price</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProviderDropdown',
  data() {
    return {
      openPDropdown: false,
    }
  }
};
</script>

<style sccoped>
.p-dropdown {
  background: #1F2B4A;
  width: 188px;
  height: 56px;
  display: flex;
  align-items: center;
  gap: 12px;
  /* position: absolute; */
}
.p-dropdown-content {
  width: 250px;
  top: 10px;
  background: #1f2b4a;
  position: absolute;
}
.e-dv {
  background: #0a1227;
  margin-bottom: 15px !important;
  padding: 7px !important;
}
</style>