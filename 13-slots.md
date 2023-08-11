# Slots

Additionally, the parent component can also pass down template fragments to the child via **slots**:
```html
<ChildComp>
    This is some slot content!
</ChildComp>
```

In the child component, it can render the slot content from the parent using the `<slot>` element as outlet:
```html
<!-- in child template -->
<slot/>
```

Content inside the `<slot>` outlet will be treated as "fallback" content: it will be displayed if the parent didn't pass down any slot content:
```vue
<slot>Fallback Content</slot>
```

<a href="https://github.com/p0chitaa/vue-training/blob/main/vue-tutorial/src/Slots.vue">Slots</a>