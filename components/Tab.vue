<template>
  <div class="tab">
      <slot></slot>
  </div>
</template>

<script>
export default {
    name: 'tab',
}
</script>

<style>
    .tab {
        width: 71px;
        height: 56px;
        background: #1F2B4A;
        border-radius: 4px;
        padding: 18px 12px;
    }

    .active-tab {
        background: #281E5D;
    }
</style>