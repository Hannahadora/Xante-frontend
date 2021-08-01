<template>
  <div id="nav">
      <ul class="flex items-center gap-10">
          <NuxtLink to="/index" class="nav-link">Home</NuxtLink>
          <NuxtLink to="/compare" class="nav-link">Compare</NuxtLink>
          <NuxtLink to="/marketAnalytics" class="nav-link">Market Analyst</NuxtLink>
          <NuxtLink to="/tools" class="nav-link">Tools</NuxtLink>
          <NuxtLink to="/opportunities" class="nav-link">Opportunities</NuxtLink>
          <NuxtLink to="/media" class="nav-link">Media</NuxtLink>
          <NuxtLink to="/contact_us" class="nav-link">Contact Us</NuxtLink>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'Nav',

}
</script>

<style>
  .nav-link {
    color: #DCE0E9;
    /* margin-right: 40px;  */
    font-size: 16px;
    font-weight: 300;
    padding: 30px 0;
  }

  #nav a.nuxt-link-exact-active {
    font-weight: 600;
    border-bottom: 4px solid #39B87D;
    padding: 30px 0;
    color: #fff;
  }
  
</style>