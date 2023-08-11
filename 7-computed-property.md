# Computed Property

> alr this is where it gets a little fucky

We're gonna continue on with the `todo` stuff from step 6. Here, this is a toggle functionality to each todo. This is done by adding a `done` property to each todo object and using `v-model` to bind it to a checkbox:
```html
<li v-for="todo in todos">
  <input type="checkbox" v-model="todo.done">
  <!-- stuff and things -->
</li>
```

So, the next big thing we can do is find a way to hide already completed `todos`. Let's create a `hideCompleted` state and make a button that toggles it. How would we render different list items based on that state?

## Introducing `computed()`
* Here we can create a computed `ref` that computes its `.value` based on other reactive data sources:
```javascript
import { ref, computed } from 'vue'

const hideCompleted = ref(false)
const todos = ref([
  /* ... */
])

const filteredTodos = computed(() => {
  // return filtered todos based on
  // `todos.value` & `hideCompleted.value`
})
```

And then change the `v-for` in the `<li>` opening tag from:
```html
<li v-for="todo in todos">
```

to:

```html
<li v-for="todo in filteredTodos">
```

Computed properties track other reactive states used in its computation as dependencies. It caches the result and automatically updates it when its dependencies change.

<a href="https://github.com/p0chitaa/vue-training/blob/main/vue-tutorial/src/ComputedProperty.vue">Computed Property</a>