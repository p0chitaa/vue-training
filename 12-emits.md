# Emits

In addition to receiving props, a child component can also emit events to the parent:
```vue
<script setup>
// declare emitted events
const emit = defineEmits(['response'])

// emit with argument
emit('response', 'hello from child')
</script>
```

The first argument to `emit()` is the event name. Any additional arguments are passed on to the event listener.

The parent can listen to child-emitted events using `v-on` - here the handler receives the extra argument from the child emit call and assigns it to local state:

```jsx
<ChildComp @response="(msg) => childMsg = msg" />
```

<a href="https://github.com/p0chitaa/vue-training/blob/main/vue-tutorial/src/Emits.vue">Emits</a>