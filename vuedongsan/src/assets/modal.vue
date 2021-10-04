<template>
    <!-- MODAL POPUP -->
    <!-- @click="modal_status = false" -->
        <div class="black-bg" v-if="modal_status == true">
            <div class="white-bg">
                <h4>{{productData[proIndex].title}}</h4>
                <img :src="productData[proIndex].image" alt="" class="room-img">
                <p>{{productData[proIndex].content}}</p>
                <p>{{productData[proIndex].price}} 만원</p>
                <Discount/>
            </div>
        </div>
        <!-- //MODAL POPUP -->
</template>

<script>
export default {
    name : "Modal",
    props : {
        proIndex : Number,
        productData : Object,
        modal_status : Boolean,
    }
}
</script>

<style>

</style>