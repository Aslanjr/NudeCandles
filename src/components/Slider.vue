<template>
    <div class="slider shadow-lg">
        <div class="container-fluid slider-item">
            <div class="row d-flex align-items-center slider-item">
                <div class="col-lg-6 col-md-6 col-sm-6 d-flex flex-column align-items-center justify-content-center ">
                    <h1 class="display-4 fw-bold">buy a candle - light the world</h1>
                    <p class=" fs-4  mt-4 fw-normal">
                        Бесплатная доставка по России при заказе от 3-х свечей
                    </p>
                </div>
                <div class="col-lg-6 col-md-6 col-sm-6 slider-item">
                    <img :src="currentImg" class="img-fluid img" alt="">
                </div>
            </div>
        </div>
    </div>    
</template>
<script>
import { mapState } from 'vuex'

export default {
  name: 'slider',
  data:()=>{
    return{
        idxSlider:1,
        crtImg:require('../assets/img/image1.png')
    }
  },
  mounted(){
      this.playSlider();
  },
  methods:{
      playSlider(){
          setInterval(() => {
             console.log(this.idxSlider);
              this.idxSlider == 3 ? this.idxSlider = 1 : this.idxSlider++;
              this.crtImg = this.listSlider[this.idxSlider].img;
          }, 2500);
      }
  },
  computed:{
    currentImg(){
        return this.crtImg
    },
    ...mapState({
      listSlider: state => state.Products.slider,
    })
  }
}
</script>
<style scoped>
    .slider-item{
        max-height: 900px;
    }
    .img{
        height: 900px;
        width: 100%;
    }
    .switch-enter-active{
        animation: Animate 1s ease-in-out;
    }
    .switch-leave-active{
        animation: Animate 1s ease-in-out reverse;
    }
    @keyframes Animate {
        0%{
            opacity: 0;
        }
        100%{
            opacity: 1;
        }
    }
</style>