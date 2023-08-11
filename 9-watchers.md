# Watchers

Here and there we may need to perform "side effects" reactively. For example, logging a number to the console when it changes:
```javascript
import { ref, watch } from 'vue'

const count = ref(0)

watch(count, (new0Count) => {
    // yes, console.log() is a side effect
    console.log(`new count is: ${newCount}`)
})
```

`watch()` can directly watch a ref, and its callback gets fired whenever `count`'s value changes. It can also watch other types of data sources.

<a href="https://github.com/p0chitaa/vue-training/blob/main/vue-tutorial/src/Watchers.vue">Watchers</a>