<template>
    <div class="quotebox">
        <h1>Quote Generator</h1>
        <div>
            <p class="quote">{{ quote.quote }}</p>
            <p class="author">-{{ quote.author }}</p>
            <button @click="emit('generate')">Another!</button>
        </div>
    </div>
</template>

<script setup>
defineProps({
    quote: {
        type: Object,
        required: true
    }
})

const emit = defineEmits(['generate'])


</script>

<style scoped>
.quotebox {
    background-color: #375a69;
    width: fit-content;
    height: 40vh;
    padding: 10px 20px;
}



.quotebox h1 {
    color: white;
    text-align: center;
}


.quotebox div {
    background-color: #c6d1d3;
    color: black;
    padding: 10px 5px;

}

.quotebox div .quote {
    font-size: 30px;
    word-wrap: break-word;
    font-weight: 900;
}

.quotebox div .author {
    text-align: right;
    font-size: 20px;
    text-transform: capitalize;
    letter-spacing: 2px;
}

.quotebox button {
    background-color: #375a69;
    color: white;
    padding: 5px;
    border: none;
    border-radius: 2px;
    cursor: pointer;
    text-align: center;


}
</style>