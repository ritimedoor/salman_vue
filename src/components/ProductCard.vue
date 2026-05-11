<script setup>

const props = defineProps({
    name: String,
    price: Number,
    img: String
})

// function beli buah
const beliBuah = () =>{
    alert(`Terima kasih, kamu telah membeli! 😁`)
}


</script>

<template>
    <div style="border: 1px solid #ccc; padding: 10px; width: 150px;">
        <img :src="img" alt="fruit image" width="100px" height="100px">
        <h3>{{ name }}</h3>
        <p>Rp {{ price }}</p>
        <button @click="beliBuah">Beli</button>

    </div>
</template>