<template>
    <div v-for="(dataP,i) in productData" :key="i">
        <img :src="productData[i].image" alt="" class="room-img">
        <h4>{{productData[i].title}}</h4>
        <p>{{productData[i].price}} 만원</p>
    </div>
</template>

<script>
export default {
    name : "Card",
    props : {
        proIndex : Number,
        productData : Object,
        modal_status : Boolean,
    }
}
</script>

<style>

</style>