# Declarative Rendering

The core feature of Vue is **declarative rendering**: using a template syntax that extends HTML, we can describe how the HTML should look like based on a JavaScript state. When the state changes, the HTML updates automatically.

States that can trigger updates when changed are considered **reactive**. We can declare reactive states using Vue's `reactive()` API. Objects created from this are JS <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy">Proxies</a> that work just like normal objects:
```javascript
import { reactive } from 'vue'

const counter = reactive ({
    count: 0
})

console.log(counter.count) // 0
counter.count++
```

`reactive()` only works on objects (including arrays and built-in tyoes like `Map` and `Set`). `ref()`, on the other hand, can take any value type and create an object that exposes teh inner value under a `.value` property:

```javascript
import { ref } from 'vue'

const message = ref('Hello World!')

console.log(message.value) // "Hello World!"
message.value = 'Changed'
```

Reactive state declared in the component's `<script setup>` block can be used directly in the template. This is how we can render dynamic text based on the value of teh `counter` object and `message` ref, using mustaches syntax:

```vue
<h1>{{ message }}</h1>
<p>count is: {{ counter.count }}</p>
```

Notice how `.value` is unnecessary when accessing the `message` ref in templates: it is automatically unwrapped from more succinct usage.

* The content inside the mustaches is not limited to just identifiers or paths -- we can use any valid JS expression:
```vue
<h1>{{ message.split('').reverse().join('') }}</h1>
```

<a href="https://github.com/p0chitaa/vue-training/blob/main/vue-tutorial/src/DeclarativeRendering.vue">Declarative Rendering</a>