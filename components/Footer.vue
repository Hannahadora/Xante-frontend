<template>
  <div id="footer">
    <div class="grid lg:grid-cols-6 md:grid-cols-3 grid-cols-2 items-start justify-between gap-10">
        <Logo class="md:col-span-1 col-span-2"/>
      <div>
          <p class="mb-10 font-bold">Product</p>
          <ul class="flex flex-col gap-4">
              <li><a class="footer-link" href="">Compare</a></li>
              <li><a class="footer-link" href="">Market Analytics</a></li>
              <li><a class="footer-link" href="">Opportunities</a></li>
              <li><a class="footer-link" href="">Media</a></li>
          </ul>
      </div>
      <div class="md:hidden block">
          <p class="mb-10 font-bold">Links</p>
          <ul class="flex flex-col gap-4">
              <li><a class="footer-link" href="">Finance Tools</a></li>
              <li><a class="footer-link" href="">Market Analytics</a></li>
              <li><a class="footer-link" href="">Opportunities</a></li>
              <li><a class="footer-link" href="">Media</a></li>
          </ul>
      </div>
      <div>
          <p class="mb-10 font-bold">Social Media</p>
          <ul class="flex flex-col gap-4">
              <li><a class="footer-link" href="">Facebook</a></li>
              <li><a class="footer-link" href="">Twitter</a></li>
              <li><a class="footer-link" href="">LinkedIn</a></li>
              <li><a class="footer-link" href="">Instagram</a></li>
          </ul>
      </div>
      <div>
          <p class="mb-10 font-bold">Contact Us</p>
         <ul class="flex flex-col gap-4">
              <li><a class="footer-link" href="">Facebook</a></li>
              <li><a class="footer-link" href="">Twitter</a></li>
              <li><a class="footer-link" href="">LinkedIn</a></li>
              <li><a class="footer-link" href="">Instagram</a></li>
          </ul>
      </div>
      <div>
          <p class="mb-10 font-bold">About Us</p>
          <ul class="flex flex-col gap-4">
              <li><a class="footer-link" href="">Facebook</a></li>
              <li><a class="footer-link" href="">Twitter</a></li>
              <li><a class="footer-link" href="">LinkedIn</a></li>
              <li><a class="footer-link" href="">Instagram</a></li>
          </ul>
      </div>
    </div>

    <p class="text-center mt-20 text-xs" style="color: #DCE0E9;">Copyright © Xante 2020</p>
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
        font-weight: 300 !important;
        width: 100%;
        padding: 80px 297px 32px 220px;
        background: #0B0F1A;  
    }

    .footer-link {
        font-weight: 300;
        font-size: 16px;
    }

    @media screen and (max-width: 1024px) {
        #footer {
             padding: 48px 24px 40px 24px;
        }
    }

    @media screen and (max-width: 768px) {
        #footer {
            padding: 48px 24px 40px 24px;
        }

        .footer-link {
            font-size: 14px !important;
        }
    }
</style>