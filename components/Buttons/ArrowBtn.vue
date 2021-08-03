<template>
  <button id="arrow-btn">
      <img src="~/assets/images/Arrowdown.png" alt="">
  </button>
</template>

<script>
export default {
     name: 'arrowbtn',
    props: ['text', 'theme']
}
</script>

<style>
    #arrow-btn {
        width: 69px;
        height: 56px;
        background: #0A1227;
        border-radius: 4px;
        padding: 25px 29px;
    }

</style>