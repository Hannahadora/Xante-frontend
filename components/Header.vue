<template>
  <div class="header flex items-center justify-between">
      <Logo />
      <Nav />
      <PryButton text="Create Account" />
  </div>
</template>

<script>
import PryButton from './Buttons/PryButton.vue'
import Logo from './Logo.vue'
import Nav from './Nav.vue'
export default {
  components: { Logo, Nav, PryButton },

}
</script>

<style>
    .header {
        height: 80px;
        width: 100%;
        border-radius: 0px;
        background: #0B0F1A;
        padding: 14px 120px;
    }

</style>