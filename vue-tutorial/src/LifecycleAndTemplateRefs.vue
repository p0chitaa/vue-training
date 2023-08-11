<script setup>
import { ref, onMounted } from 'vue'

const pElementRef = ref(null)

onMounted(() => {
    pElementRef.value.textContent = "this text has been changed from 'hello'!"
})
</script>

<template>
    <p ref="pElementRef">hello</p>
</template>