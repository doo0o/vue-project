<template>
    <div>
        <div class="menu">
                <a v-for="gnb in gnbList" :key="gnb">{{gnb}}</a>
        </div>

        <Discount/>

        <!-- MODAL POPUP -->
        <Modal @closeModal="modal_status= false" :productData = "productData" :proIndex = "proIndex" :modal_status = "modal_status" />
        <!-- //MODAL POPUP -->
       
        <!-- Contents -->
        <Card @openModal="modal_status=true;proIndex = $event" :productData="productData[i]" :modal_status="modal_status" v-for="(datalength,i) in productData" :key="datalength" />
        <!-- //Contents -->
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
            object : {name : 'jeong' , age : '27'},
            proIndex : 0,
            productData : data,
            modal_status : false,
            gnbList : ['HOME','SHOP','ABOUT']
        }
    },
    components: {
        Discount : Discount,
        Modal : Modal,
        Card : Card,
    }
}
</script>
<style src="./common.css"></style>

