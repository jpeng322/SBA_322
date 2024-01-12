<template>
  <button v-on:click="onClick()" :style="{ backgroundColor: color }">
    {{ buttonName }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    buttonName: String,
    color: String,
  },
  methods: {
    onClick() {
      alert("This is an alert message!");
    },
  },
};
</script>
