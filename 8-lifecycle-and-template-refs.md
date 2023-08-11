# Lifecycle and Template Refs

Up to now, Vue has been handling all the DOM updates for us,, shoutout declarative rendering and reactivity. But there will be cases where we need to manually work with the DOM.

We can request a **template ref** - aka a reference to an element in the template - using the `ref` attribute:
```html
<p ref="pElementRef">hello</p>
```

To access this ref, we need to declare a ref with a matching name:
```javascript
const pElementRef = ref(null)
```

Note that the ref is initialized with a `null` value; this is only because the element itself doesn't yet exist when `<script setup>` is executed. The template ref is only accessible after the component is **mounted**.

To run the code after mount, just use the `onMounted()` function:
```javascript
import { onMounted } from 'vue'

onMounted(() => {
    // component is now mounted! ;))
})
```

This is what is known as a **lifecycle hook** - it lets us register a callback to be called at certain times of the component's lifecycle. There are other hooks such as `onUpdated` and `onUnmounted`. See the <a href="https://vuejs.org/guide/essentials/lifecycle.html#lifecycle-diagram">Lifecycle Diagram</a> for more.

<a href="https://github.com/p0chitaa/vue-training/blob/main/vue-tutorial/src/LifecycleAndTemplateRefs.vue">Lifecycle and Template Refs</a>