<template>
    <div>
        <div class="menu">
                <a v-for="gnb in gnbList" :key="gnb">{{gnb}}</a>
        </div>

        <Discount/>

        <!-- MODAL POPUP -->
        <Modal :productData = "productData" :proIndex = "proIndex" :modal_status = "modal_status" />
        <!-- //MODAL POPUP -->
       
        <!-- Contents -->
        <Card :productData = "productData" :proIndex = "proIndex" :modal_status = "modal_status"/>
        <!-- //Contents -->

        <!-- BackUp -->
        <!-- <div v-for="(dataP,i) in productData" :key="i">
            <img :src="productData[i].image" alt="" class="room-img">
            <h4 @click="modal_status = true;proIndex = i;">{{productData[i].title}}</h4>
            <p>{{productData[i].price}} 만원</p>
        </div> -->
        <!-- //BackUp -->
    </div>
</template>

<script>

import data from './assets/dataPro.js';
import Discount from './assets/discount.vue';
import Modal from './assets/modal.vue';
import Card from './assets/card.vue';

export default{
    name : 'app',
    data(){
        return{
            proIndex : 0,
            productData : data,
            modal_status : false,
            gnbList : ['HOME','SHOP','ABOUT']
        }
    },
    components: {
        Discount,
        Modal,
        Card,
    }
}
</script>
<style src="./common.css"></style>

