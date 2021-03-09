<template>
    <div class="footer bg-danger">
        <div class="container">
            <div class="row d-flex justify-content-around">
                <div class="col-lg-6 d-flex justify-content-start">
                    <h1 class="logo text-center">Nude <br> Candles</h1>
                </div>
                <div class="col-lg-6 d-flex justify-content-start align-items-center flex-column">
       
                    <div class="menu__title">Мы в соц сетях</div>
                    <div class="d-flex">
                        <img src="../assets/media/facebook.png" class="img " alt="">
                        <img src="../assets/media/instagram.png" class="img">
                        <img src="../assets/media/whatsapp.png" class="img">
                    </div>
                </div>
                <div class="col-lg-12 d-flex justify-content-center">
                    <p class="link">Powered by AslanJr</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name:'footer',
    data:()=>{
        return{

        }
    }    
}
</script>
<style scoped>
  .footer{
      padding: 3% 0% 0% 0%;
  }
  .logo{
    font-family: 'Akaya Telivigala', cursive;
    font-size: 60px;
    color: rgb(221, 197, 161);
  }
  .menu__title{
    font-family: 'Akaya Telivigala', cursive;
    font-size: 35px;
    transition: all .45s ease-in-out;
    cursor: pointer;
    color: rgb(221, 197, 161);
  }
  .link{
    font-family: 'Akaya Telivigala', cursive;
    font-size: 19px;
    cursor: pointer;
    color: rgb(221, 197, 161);
  }
  .img{
      margin: 10px 10px;
      transition: all .45s ease-in-out;
      cursor: pointer;
  }
  .img:hover{
      transform: scale(1.5) rotate(5deg);
  }
</style>