<template>
  <div class="mainPage">
    <Carousel/>
    <ProductPanel title="Top Selling" section="topselling" />
    
    
  </div>
</template>

<script>
import ProductPanel from './ProductPanel.vue'
import Carousel from './Carousel.vue'


export default {
  name: 'MainPage',
  components: {
    ProductPanel,
    Carousel
  }
}
</script>

<style></style>
