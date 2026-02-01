<template>
  <div>

    <!-- <BaseFacts/> -->

    <!-- <BaseList :users="users" /> -->

    <BaseProducts/>

  </div>
</template>

<script setup>
import BaseFacts from '@/components/BaseFacts.vue';
import BaseList from '@/components/BaseList.vue';
import BaseProducts from './components/BaseProducts.vue';

const users = [
  {
    id: 1,
    name: "John Doe",
    role: "Admin",
    active: true
  },
  {
    id: 2,
    name: "Jane Smith",
    role: "Editor",
    active: false
  },
  {
    id: 3,
    name: "Mike Johnson",
    role: "Viewer",
    active: true
  }
]

</script>

<style lang="scss" scoped></style>