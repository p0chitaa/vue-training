# Event Listeners

We can listen to DOM events using the `v-on` directive:

```html
<button v-on:click="increment">{{ count }}</button>
```

Here, `increment` is referencing a function declared in `<script setup>`

```html
<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
  // update component state
  count.value++
}
</script>
```

Inside the function, we can update the component state by mutating refs.

Event handlers can also use inline expressions, and can simplify common tasks with modifiers.

<a href="https://github.com/p0chitaa/vue-training/blob/main/vue-tutorial/src/EventListeners.vue">Event Listeners</a>