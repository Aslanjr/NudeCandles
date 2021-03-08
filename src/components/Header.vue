<template>
  <div class="header bg-light shadow-lg">
    <div class="container">
      <div class="row d-flex align-items-center">
        <div class="col-lg-5 d-flex justify-content-center menu__title">
          Главная
        </div>
        <div class="col-lg-2 mr-5 ml-5">
          <h1 class="logo text-center">Nude <br> Candles</h1>
        </div>
        <div class="col-lg-5 d-flex justify-content-center text-left menu__title">
          О нас
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import { mapState } from 'vuex'

export default {
  name: 'header',
  data:()=>{
    return{

    }
  },
  computed:{
    msg(){
      console.log(this.listProduct)
      return 'this.listProduct'
    },
    ...mapState({
      listProduct: state => state.Products.allProducts,
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .logo{
    font-family: 'Akaya Telivigala', cursive;
    font-size: 60px;
  }
  .menu__title{
    font-family: 'Akaya Telivigala', cursive;
    font-size: 35px;
    transition: all .45s ease-in-out;
    cursor: pointer;
  }
  .menu__title:hover,.logo{
    color: rgb(221, 197, 161);
  }
</style>
