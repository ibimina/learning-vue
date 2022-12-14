<template>
  <div class="template-refs">
    <div>
      <h1>Change text using template refs with Event listeners</h1>
      <p>{{ text }}</p>
      <p ref="events" class="mouse-event">hi</p>
      <div class="mouse-wrapper">
        <button @mousedown="handlemouse('mouse down')">mouse down</button>
        <button @mouseup="handlemouse('mouse up')">mouse up</button>
        <button @mouseenter="handlemouse('mouse enter')">mouse enter</button>
        <button @mouseleave="handlemouse('mouse leave')">mouse leave</button>
        <button @mousemove="handlemouse('mouse move')">mouse move</button>
      </div>
    </div>

    <div>
      <h1>Change text using Event listeners</h1>
      <p>State mangement in vue</p>
      <p class="mouse-event">{{ data }}</p>
      <div class="mouse-wrapper">
        <button @mousedown="handleevent('mouse down')">mouse down</button>
        <button @mouseup="handleevent('mouse up')">mouse up</button>
        <button @mouseenter="handleevent('mouse enter')">mouse enter</button>
        <button @mouseleave="handleevent('mouse leave')">mouse leave</button>
        <button @mousemove="handleevent('mouse move')">mouse move</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return { text: "mouse events", data: "data state " };
  },
  methods: {
    handlemouse(word) {
      this.$refs.events.textContent = word;
    },
    handleevent(word) {
      this.data = word;
    },
  },
};
</script>
