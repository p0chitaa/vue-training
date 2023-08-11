<script setup>
import { ref } from 'vue'
import SlotsComp from './components/SlotsComp.vue'

const msg = ref('from parent')
</script>

<template>
  <ChildComp>Message: {{ msg }}</ChildComp>
</template>