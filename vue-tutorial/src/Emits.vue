<script setup>
import { ref } from 'vue'
import EmitsComp from './components/EmitsComp.vue'

const childMsg = ref('No child msg yet')
</script>

<template>
  <EmitsComp @response="(msg) => childMsg = msg" />
  <p>{{ childMsg }}</p>
</template>