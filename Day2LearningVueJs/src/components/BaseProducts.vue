<template>
    <div>
        <h1>Hello Lordsainath</h1>


        <p v-if="loading">Loading Products...</p>
        <p v-else-if="error">{{ error }}</p>

        <!-- Empty -->
        <p v-else-if="products.length === 0">No products found</p>

        <ul class="box1" v-else v-for="products in products" :key="products.id">
            <p>Your Id is : {{ products.id }}</p>
            <p>Your Product Category is : {{ products.category }}</p>
            <p>Your Product Title is : {{ products.title }}</p>
            <p>Your Product Price is : {{ products.price }}</p>
        </ul>


    </div>
</template>

<script setup>
import { onMounted, ref } from 'vue';


onMounted(async () => {

    const data = await fetch('https://fakestoreapi.com/products/')
        .then(source => source.json())
        .then(data => {
            products.value = data
            loading.value = false
        }).catch(err => {
            error.value = err.message
            loading.value = false
        })

})


const products = ref([])
const loading = ref(true)
const error = ref(null)




</script>

<style  scoped>
.box1 {
    background-color: gray;
    color: black;
    padding: 5px 10px;
    border-radius: 5px;
}
</style>