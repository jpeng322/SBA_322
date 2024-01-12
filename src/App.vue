<script setup>
import Header from "./components/Header.vue";
import Button from "./components/Button.vue";

const vHighlight = {
  mounted(el) {
    el.style.backgroundColor = "yellow";
  },
};


</script>

<template>

  <Header />
  <Button buttonName="This Button Alerts" color="red" />
  <div>
    <h2>This input message will be displayed on the bottom of the page.</h2>
    <input v-model="message" />
  </div>
  <div class="spacer"></div>
  <p>Here is your message.</p>
  <p  v-highlight>{{ message }}</p>
</template>

<script>
export default {
  data() {
    return {
      message: "Type a message",
    };
  },
};
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

.message {
  font-size: 1.5rem;
  font-weight: bold;
  background-color: yellow;
}

.spacer {
  height: 2000px;
}
</style>
