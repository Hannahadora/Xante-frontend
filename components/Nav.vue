<template>
  <div class="top-nav">
      <ul class="flex items-center gap-10">
          <NuxtLink to="/" class="top-nav-link">Home</NuxtLink>
          <NuxtLink to="/compare" class="top-nav-link">Compare</NuxtLink>
          <NuxtLink to="/marketAnalytics" class="top-nav-link">Market Analyst</NuxtLink>
          <NuxtLink to="/tools" class="top-nav-link">Tools</NuxtLink>
          <NuxtLink to="/opportunities" class="top-nav-link">Opportunities</NuxtLink>
          <NuxtLink to="/media" class="top-nav-link">Media</NuxtLink>
          <NuxtLink to="/contact" class="top-nav-link">Contact Us</NuxtLink>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'Nav',

}
</script>

<style>
  .top-nav-link {
    color: #DCE0E9;
    /* margin-right: 40px;  */
    font-size: 16px;
    font-weight: 300;
  }

  .top-nav-link-exact {
    font-weight: 600;
  }
  
</style>