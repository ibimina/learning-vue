<template>
  <div class="about">
    <h1>Event listeners using template refs</h1>
    <p>{{ text }}</p>
    <p ref="events">hi</p>
    <button @mousedown="handlemouse('mouse down')">mouse down</button>
    <button @mouseup="handlemouse('mouse up')">mouse up</button>
    <button @mouseenter="handlemouse('mouse enter')">mouse enter</button>
    <button @mouseleave="handlemouse('mouse leave')">mouse leave</button>
    <button @mousemove="handlemouse('mouse move')">mouse move</button>
  </div>
</template>

<script>
export default {
  data() {
    return { text: "mouse events" };
  },
  methods: {
    handlemouse(word) {
      this.$refs.events.textContent = word;
    },
  },
};
</script>
