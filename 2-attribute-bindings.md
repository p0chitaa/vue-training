In vue, mustaches are only used for text interpolation. To bind an attribute to
a dynamic value, we use the `v-bind` directive:

```html
<div v-bind:id="dynamicId"></div>
```

A directive is a special attribute that starts with the `v-` prefix. They are part of Vue's template syntax. Similar to text interpolations, directive values are JavaScript
expressions that have access to the component's state. 

The part after the color `:id` is the "argument" of the directive. Here, the element's
`id` attribute will be synced with the `dynamicId` property from the component's state.

Because `v-bind` is used to frequently, it has a dedicated shorthand syntax:

```html
<div :id="dynamicId"></div>
```

<a href="https://github.com/p0chitaa/vue-training/blob/main/vue-tutorial/src/DeclarativeRendering.vue">Attribute Bindings</a>