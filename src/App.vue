<script setup>
import { ref } from "vue"
import ProductCard from "./components/ProductCard.vue";


// tempat naro buah
const fruits = ([
  {id: 1, name:"Apple", price:15000, img:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ0YETDAhJ_H3sFqZBTQYQ1GefQR9FGaVgMjQ&s"},
  {id: 2, name:"Orange", price:25000, img:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSlwhljHF53Gin9MFEnKeb-PmmE4JsfY_1HSA&s"},
  {id: 3, name:"Snake Fruit", price:5000, img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ0YETDAhJ_H3sFqZBTQYQ1GefQR9FGaVgMjQ&s"},

])

const username = ref("")

</script>

<template>

  <div style="padding: 20px; background-color: aquamarine;">
    <h1>MARI MAKAN BUAH SEGAR! </h1>
    
    <input type="text" v-model="username" placeholder="masukkan nama kamu lur..." />
    <p>Halo! {{ username }}, kamu pasti mau beli buah kan?!</p>

    <hr /> 

  

  <div style="display: flex; gap: 10px; flex-wrap: wrap;">
    <ProductCard
    v-for="item in fruits"
    :key="item.id"
    :name="item.name"
    :price="item.price"
    :img="item.img"
    >


    </ProductCard>

  </div>

  </div>



</template>
