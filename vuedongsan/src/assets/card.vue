<template>
    <div>
        <img :src="productData.image" alt="" class="room-img">
        <h4 @click="factory();">{{productData.title}}</h4>
        <p>{{productData.price}} 만원</p>
    </div>
</template>

<script>
export default {
    name : "Card",
    props : {
        // proIndex : Number,
        productData : Object,
        modal_status : Boolean,
    },
    methods: {
        factory(){
            this.$emit('openModal',this.productData.id)
        }
    },
}
</script>

<style>
 
</style>