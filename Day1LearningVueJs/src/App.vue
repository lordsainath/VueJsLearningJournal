<template>

  <h1>Hello {{ name }}</h1>

  <button @click="UpdateNameToOriginal"> Change To Original</button>

  <BaseButton @changeText="UpdateName" content="Change Name" />


  <Counter :count="count" @increment="increment" @decrement="decrement" @reset="reset" />

</template>

<script setup>
import { ref } from 'vue'
import BaseButton from './components/BaseButton.vue';
import Counter from './components/Counter.vue';

const name = ref('Sainath')

const count = ref(0)

function UpdateNameToOriginal() {
  name.value = 'Sainath'
}

function UpdateName(data) {

  name.value = data
}


function increment(data = 1) {
  if (data) {
    count.value += data
  } else {

    count.value++
  }


}

function decrement(data = 1) {

  if (count.value <= 0) {
    alert('number cannot be negative')
  } else {

    count.value -= data
  }
}

function reset() {
  count.value = 0
}

</script>

<style lang="scss" scoped></style>