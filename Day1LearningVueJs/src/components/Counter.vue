<template>
    <div>
        <p>Counter : {{ count }}</p>


        <input v-model.number="numData" placeholder="Operations by value" type="number" />

        <div class="btngroup">


            <button @click="emit('increment', numData)">Increment</button>
            <button @click="emit('decrement', numData)">Decrement</button>
            <button @click="emit('reset')">Reset</button>


        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
const numData = ref(1)

defineProps({
    count: {
        type: Number,
        default: 0
    }
})

const emit = defineEmits(['increment', 'decrement', 'reset'])
</script>

<style scoped>
.btngroup {
    display: flex;
    gap: 4px;
}
</style>