<template>
  <div id="media">
      <Header />
        <div class="">
            <div class="media-intro">
                <h2 class="sharp mb-36">Media</h2>
            </div>
            <div class="media-view">
                <div class="media-box" style="background: #938D8D; height: 938px"></div>
                <div class="media-box" style="background: #BCAAAA;"></div>
                <div class="media-box" style="background: #393232; height: 698px"></div>
                <div class="media-box" style="background: #BCAAAA;"></div>
                <div class="media-box" style="background: #BCAAAA;"></div>
                <div class="media-box" style="background: #BCAAAA;"></div>
                <div class="media-box" style="background: #BCAAAA;"></div>
                <div class="media-box" style="background: #BCAAAA;"></div>
                <div class="media-box" style="background: #BCAAAA;"></div>
            </div>
        </div>
      <Footer />
  </div>
</template>

<script>
import Footer from '~/components/Footer.vue'
import Header from '~/components/Header.vue'
export default {
  components: { Header, Footer },
    name: 'Media'

}
</script>

<style>
    .media-intro {
        margin: 120px 120px 143px 120px;
    }

    .media-view {
        margin-bottom: 163px;
        display: grid;
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }  
    .media-box {
        height: 486px;
        width: 100%;
    }

</style>