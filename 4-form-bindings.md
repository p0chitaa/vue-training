# Form Bindings

Using `v-bind` and `v-on` together, we can create two-way bindings on form input elements:
```html
<input :value="text" @input="onInput">
```
```javascript
function onInput(e) {
    // a v-on handler receives the native DOM event
    // as the argument
    text.value = e.target.value
}
```

To simplify two-way bindings, Vue provides a directive, `v-model`, which is essentially a syntax sugar for the above:
```html
<input v-model="text">
```

`v-model` automatically sync the `<input>`'s value with the bound state, so we no longer need to use an event handler for that.

`v-model` works not only on text inputs, but also on other input types such as checkboxes, radio buttons, and select dropdowns.

<a href="https://github.com/p0chitaa/vue-training/blob/main/vue-tutorial/src/FormBindings.vue">Form Bindings</a>