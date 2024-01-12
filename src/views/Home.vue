<script setup>
import Header from "../components/Header.vue";
import Button from "../components/Button.vue";

const vHighlight = {
  mounted(el) {
    el.style.backgroundColor = "yellow";
  },
};

const vBig = {
  mounted(el) {
    el.style.fontSize = "50px";
  },
};
</script>

<template>
  <div class="homepage" v-big>This is the homepage.</div>

  <Header />
  <Button buttonName="This Button Alerts" color="red" />
  <div>
    <h2>This input message will be displayed on the bottom of the page.</h2>
    <input v-model="message" />
  </div>
  <div class="spacer"></div>
  <p>Here is your message.</p>
  <p class="message" v-highlight>{{ message }}</p>
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
.message {
  font-size: 2rem;
  font-weight: bold;
  background-color: yellow;
  padding: 0;
  margin: 0;
}

.spacer {
  height: 2000px;
}
</style>
