<template>
  <div id="login-page">
    <Logo class="mx-auto pt-20"/>
    <div class="login-box text-center mx-auto">
        <h2>Log in to Xante</h2>
        <p class="mt-4 mb-12">A short caption text here. Could be why Xante or a feature or a reason etc.</p>
        <div class="rect9 mb-8 flex items-center justify-center">
            <img class="mr-3" src="../assets/images/Google.png" alt="">
            <p class="text-black font-semibold">Sign up with Google</p>
        </div>
        <div class="rect9 flex items-center justify-center">
            <img class="mr-3" src="../assets/images/Facebook.png" alt="">
            <p class="text-black font-semibold">Sign up with Facebook</p>
        </div>  

        <NuxtLink to="/signup" class="mt-12">
            <span>Don't have an account? </span><span class="font-bold">Sign Up</span>
        </NuxtLink>   
    </div>
</div>
  
</template>

<script>
import Logo from '~/components/Logo.vue'
export default {
    name: 'Signup',
  components: { Logo },

}
</script>

<style>
h2 {
    font-family: Mulish;
    font-size: 32px;
    font-style: normal;
    font-weight: 600;
    line-height: 40px;
}
</style>