<template>
  <div class="relative">
    <div>
      <img
        class="img1 xl:block hidden mx-auto pt-20"
        src="/images/logo.png"
        alt=""
      />
    </div>

    <signup-vue />
    <div class="absolute bottom-0 right-0">
      <img src="/images/first.png" alt="" />
    </div>
  </div>
</template>

<script>
import signupVue from "~/components/signup.vue";

export default {
  name: "Login",
  components: { signupVue },
  layout: "form",
};
</script>

<style scoped>
</style>