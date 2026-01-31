<template>
    <div>
        <button @click="emit('changeText','lordsainath is here')">{{ content }}</button>
    </div>
</template>

<script setup>
defineProps({
    content: {
        type: String,
        default: 'button'
    }
})

const emit = defineEmits(['changeText'])

</script>

<style lang="scss" scoped></style>