<template>
    <div>
        <h1>User List</h1>
        <ul>
            <li v-for="user in users" :key="user.id">
                <p>Id : {{ user.id }}</p>
                <p>Name : {{ user.name }}</p>
                <p>Role : {{ user.role }}</p>
                <p>IsActive : {{ user.active }}</p>
            </li>
        </ul>
    </div>
</template>

<script setup>
defineProps({
    users: {
        type: Array,
        required: true
    }
})

</script>

<style lang="scss" scoped></style>