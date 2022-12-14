<script>
export default {
  data() {
    return {
      count: 1,
    };
  },
  methods: {
    increment() {
      return this.count++;
    },
    decrement() {
      return this.count--;
    },
  },
};
</script>

<template>
  <h1>Counter</h1>
  <p>{{ count }}</p>
  <button @click="increment">+</button>
  <button @click="decrement" :disabled="count < 1">-</button>
</template>
