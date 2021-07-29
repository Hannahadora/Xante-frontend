<template>
  <div id="footer">
    <div class="flex items-start justify-between">
        <Logo />
      <div>
          <p class="mb-10 font-bold">Product</p>
          <ul class="flex flex-col gap-4">
              <li class="footer-link">Compare</li>
              <li class="footer-link">Market Analytics</li>
              <li class="footer-link">Opportunities</li>
              <li class="footer-link">Media</li>
          </ul>
      </div>
      <div>
          <p class="mb-10 font-bold">Social Media</p>
          <ul class="flex flex-col gap-4">
              <li class="footer-link">Facebook</li>
              <li class="footer-link">Twitter</li>
              <li class="footer-link">LinkedIn</li>
              <li class="footer-link">Instagram</li>
          </ul>
      </div>
      <div>
          <p class="mb-10 font-bold">Contact Us</p>
         <ul class="flex flex-col gap-4">
              <li class="footer-link">Facebook</li>
              <li class="footer-link">Twitter</li>
              <li class="footer-link">LinkedIn</li>
              <li class="footer-link">Instagram</li>
          </ul>
      </div>
      <div>
          <p class="mb-10 font-bold">About Us</p>
          <ul class="flex flex-col gap-4">
              <li class="footer-link">Facebook</li>
              <li class="footer-link">Twitter</li>
              <li class="footer-link">LinkedIn</li>
              <li class="footer-link">Instagram</li>
          </ul>
      </div>
    </div>

    <p class="text-center mt-20 text-xs">Copyright © Xante 2020</p>
  </div>
</template>

<script>
import Logo from './Logo.vue'
export default {
  components: { Logo },

}
</script>

<style>
    #footer {
        width: 100%;
        padding: 80px 297px 32px 220px;
        background: #0B0F1A;   
    }

    .footer-link {
        font-weight: 300;
    }

</style>