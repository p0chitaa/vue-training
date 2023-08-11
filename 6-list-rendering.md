# List Rendering

We can use the `v-for` directive to render a list of elements based on a source array:
```html
<ul>
  <li v-for="todo in todos" :key="todo.id">
    {{ todo.text }}
  </li>
</ul>
```

Here, todo basically `todo` is a local variable that represents the array element currently being iterated on. Only accessible on or inside the `v-for` element.

Also, here we are giving each todo object a unique `id`, and binding it as the `key` attribute for each `<li>`. This allows Vue to move each `<li>` to match the position of its corresponding object in the array.

Two ways to update the list:
1. Call <a href="https://stackoverflow.com/questions/9009879/which-javascript-array-functions-are-mutating">mutating methods</a> on the source array:
```javascript
todos.value.push(newTodo)
```

2. Orrrrr replace the array with a new one:
```javascript
todos.value = todos.value.filter(/* stuff and things */)
```

<a href="https://github.com/p0chitaa/vue-training/blob/main/vue-tutorial/src/ListRendering.vue">List Rendering</a>