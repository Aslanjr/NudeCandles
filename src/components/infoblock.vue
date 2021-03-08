<template>
    <div class="infoblock">
        <div class="container">
            <div class="row d-flex flex-column align-items-center">
                <div class="col-lg-2 w-100 mb-5 mt-5 text-center">
                    <h2 class="info__title">Наш план работы</h2>
                </div>
                <div class="col-lg-10 col-md-10 col-sm-10 mw-100 mt-2 d-flex justify-content-around">
                    <div class="col-lg-4 col-md-4 col-sm-4 d-flex flex-column align-items-center text-center info__item">
                        <img :src="icon[0].img" alt="">
                        <h1 class="info__text">СОСТАВ</h1>
                        <p >Наши свечи изготовлены из 100% органического соевого воска с использованием хлопкового фитиля и ароматизаторов с добавлением эфирных масел</p>
                    </div>
                    <div class="col-lg-4 col-md-4 col-sm-4 d-flex flex-column align-items-center text-center info__item">
                        <img :src="icon[1].img" alt="">
                        <h1 class="info__text">УПАКОВКА</h1>
                        <p>Бумага тишью, транспортировочная пленка, бумажный наполнитель и коробочка позаботятся о надежности доставки</p>
                    </div>
                    <div class="col-lg-4 col-md-4 col-sm-4 d-flex flex-column align-items-center text-center info__item">
                        <img :src="icon[2].img" alt="">
                        <h1 class="info__text">ДОСТАВКА</h1> 
                        <p>Мы отправляем наши свечи по всему миру, а при заказе от 3-х свечей доставка по России за наш счёт</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name:'infoblock',
    data:()=>{
        return{
            icons:[
                {
                    img:require('../assets/icons/decentralized.png'),
                },
                {
                    img:require('../assets/icons/box.png'),
                },
                {
                    img:require('../assets/icons/delivery.png')
                }
            ]
        }
    },
    
    computed:{
        icon(){
            return this.icons;
        }
    }
}
</script>
<style scoped>
    .info__title{
        font-family: 'Akaya Telivigala', cursive;
        font-size: 45px;
        color:rgb(221, 197, 161);
    }
    .info__text{
        font-family: 'Akaya Telivigala', cursive;
        font-size: 25px;
        color:rgb(221, 197, 161);
        margin: 40px 0px 30px 0px;
    }
    .info__item{
        border-right: 1px solid black;
        padding: 0px 20px;
    }
    .info__item:nth-child(3){
        border-right: none;
    }
</style>