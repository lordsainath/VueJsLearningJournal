<template>
  <div>
    <h1>Hello Sainath Welcome to Day 3 of Vue.js Learning Journal</h1>

    <BaseQuoteGenerator :quote="quote" @generate="generateRandomeQuote" />

  </div>
</template>

<script setup>
import BaseQuoteGenerator from './components/BaseQuoteGenerator.vue';

import { onMounted, ref } from 'vue';


const quotes = [
  {
    quote: "Be yourself; everyone else is already taken.",
    author: "Oscar Wilde"
  },
  {
    quote: "In the middle of difficulty lies opportunity.",
    author: "Albert Einstein"
  },
  {
    quote: "Do what you can, with what you have, where you are.",
    author: "Theodore Roosevelt"
  },
  {
    quote: "Simplicity is the ultimate sophistication.",
    author: "Leonardo da Vinci"
  },
  {
    quote: "Stay hungry, stay foolish.",
    author: "Steve Jobs"
  },
  {
    quote: "Happiness depends upon ourselves.",
    author: "Aristotle"
  },
  {
    quote: "Dream big and dare to fail.",
    author: "Norman Vaughan"
  }
];

const quote = ref({});



function generateRandomeQuote() {
  let randomNumber = Math.floor(Math.random() * quotes.length);
  quote.value = quotes[randomNumber]

}

onMounted(() => {
  generateRandomeQuote()
})



</script>

<style lang="scss" scoped></style>