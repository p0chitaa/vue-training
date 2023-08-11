# Components

As of right now, we've only been working with a single component. Real Vue apps usually have nested components.

A parent component can render another component in its template as a child component. To use a child component, we need to import it first:
```javascript
import ChildComp from './ChildComp.vue'
```

And then we can use it in the template as:
```jsx
<ChildComp />
```

<a href="https://github.com/p0chitaa/vue-training/blob/main/vue-tutorial/src/Components.vue">Components</a>