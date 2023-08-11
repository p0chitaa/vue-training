# Conditional Rendering

We can use the `v-if` directive to conditionally render an element:
```html
<h1 v-if="awesome">Vue is awesome!</h1>
```

This `<h1>` will be rendered only if the value of `awesome` is <a href="https://developer.mozilla.org/en-US/docs/Glossary/Truthy">truthy</a>. If `awesome` changes to a <a href="https://developer.mozilla.org/en-US/docs/Glossary/Falsy">falsy</a> value, it will be removed from the DOM.

We can also use `v-else` and `v-else-if` to denote other branches of the condition:
```html
<h1 v-if="awesome">Vue is awesome!</h1>
<h1 v-else>Oh no 😢</h1>
```

<a href="https://github.com/p0chitaa/vue-training/blob/main/vue-tutorial/src/ConditionalRendering.vue">Conditional Rendering</a>