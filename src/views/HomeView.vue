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
  <div class="home-container">
    <h1>Counter</h1>
    <p class="count">{{ count }}</p>
    <div class="mouse-wrapper">
      <button @click="increment" class="btn">+</button>
      <button @click="decrement" :disabled="count < 1" class="btn">-</button>
    </div>
  </div>
</template>
