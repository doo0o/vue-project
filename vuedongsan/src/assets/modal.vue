<template>
    <!-- MODAL POPUP -->
    <!-- @click="modal_status = false" -->
        <div class="black-bg" v-if="modal_status == true">
            <div class="white-bg">
                <h4>{{productData[proIndex].title}}</h4>
                <img :src="productData[proIndex].image" alt="" class="room-img">
                <p>{{productData[proIndex].content}}</p>
                <input type="text" v-model.number="month">
                <!-- @input="month = $event.target.value" -->
                <p>{{month}}개월</p>
                <p>{{productData[proIndex].price*month}} 만원</p>
                <Discount/>
                <button @click="closeModal()">닫기</button>
            </div>
        </div>
        <!-- //MODAL POPUP -->
</template>

<script>
import Discount from './discount.vue';
export default {
    name : "Modal",
    props : {
        proIndex : Number,
        productData : Object,
        modal_status : Boolean,
    },
    data(){
        return{
            month : 1,
        }
    },
    watch : {
        month(a){
            if(a >= 13){
                alert('13개월 이상은 입력하실 수 없습니다.')
            }
        }
    },
    methods: {
        closeModal(){
            this.$emit('closeModal');
            console.log('------------Close Modal');
        }
    },
    components : {
        Discount : Discount,
    }
}
</script>

<style>

</style>