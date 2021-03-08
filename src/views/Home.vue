<template>
  <div class="home">
    <Header />
    <Slider/>
    <Infoblock/>
    <Products/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '../components/Header.vue'
import Slider from '../components/Slider.vue'
import Infoblock from '../components/infoblock.vue'
import Products from '../components/products.vue'

export default {
  name: 'Home',
  components: {
    Header,
    Slider,
    Infoblock,
    Products
  }
}
</script>
