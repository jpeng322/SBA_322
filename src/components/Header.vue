<template>
  <header>
    <h1>This is a simple header.</h1>
    <h1
      v-bind:class="{
        italic: true,
        isGreen: true,
      }"
    >
      This is a italicized green header.
    </h1>
  </header>

</template>

<script>
</script>

<style scoped>
header {
  border: 2px solid black;
  padding: 1rem;
  margin-bottom: 2rem;
  border-radius: 0.5rem;
  .italic {
    font-style: italic;
  }
  .isGreen {
    color: forestgreen;
  }
}
</style>
