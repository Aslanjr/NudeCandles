<template>
    <div class="products shadow-lg">
        <div class="container mt-5">
            <div class="row">
                <div class="product__title text-center mt-5">КАТАЛОГ</div>
                <div class="row d-flex">
                    <div class="col-lg-4 col-md-4 col-sm-4" v-for="(item,index) in listProducts" :key="index">
                        <div class="card mb-3">
                            <img :src="item.img" class="card-img-top img-fluid img">
                            <div class="card-body">
                                <h5 class="card-title">{{item.title}}</h5>
                                <p class="card-text">{{item.description}}</p>
                                <p class="card-text">Цена: {{item.amount}} тг. </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>

import { mapState } from 'vuex'

export default {
    name:'infoblock',
    data:()=>{
        return{
            
        }
    },
    computed:{
        ...mapState({
            listProducts: state => state.Products.allProducts
        })
    }
}
</script>
<style scoped>
    .product__title{
        font-family: 'Akaya Telivigala', cursive;
        font-size: 45px;
        color:rgb(221, 197, 161);
    }
    .img{
        height: 500px;
    }
</style>