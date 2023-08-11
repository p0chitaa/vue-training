<script setup>
import { ref } from 'vue'
import PropsComp from './components/PropsComp.vue'

const greeting = ref('Hello from parent!')
</script>

<template>
  <PropsComp :msg="greeting" />
</template>