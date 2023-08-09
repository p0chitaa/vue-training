<script setup>
import { ref } from 'vue'
import { reactive } from 'vue'

/*
The core feature of Vue is declarative rendering: using a template syntax 
that extends HTML, we can describe how the HTML should look like based on 
JavaScript state. When the state changes, the HTML updates automatically.
*/

/*
States that can trigger upadtes when changed are considered REACTIVE.
We can declare reactive state using Vue's `reactive()` API. Objects
created from `reactive()` are JavaScript Proxies that work just like
normal objects.
*/

const counter = reactive({ count: 0 })

console.log(counter.count) // 0
counter.count++

const message = ref('Hello World!')

console.log(message.value) // "Hello World!""
message.value = 'Changed'
</script>

<template>
    <h1>{{ message }}</h1>
    <p>count is: {{ counter.count }}</p>
</template>