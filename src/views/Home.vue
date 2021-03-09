<template>
  <div class="home">
    <Header />
    <Slider/>
    <Infoblock/>
    <Products/>
    <Message/>
    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '../components/Header.vue'
import Slider from '../components/Slider.vue'
import Infoblock from '../components/infoblock.vue'
import Products from '../components/products.vue'
import Message from '../components/message.vue';
import Footer from '../components/footer.vue'

export default {
  name: 'Home',
  components: {
    Header,
    Slider,
    Infoblock,
    Products,
    Message,
    Footer
  }
}
</script>
