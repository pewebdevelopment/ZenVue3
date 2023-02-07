<template>
  <div>{{ greet }} {{ name }}</div>
  <div v-text="channel"></div>
  <div v-html="channel2"></div>
</template>

<script>
export default {
  name: "Binding-v-bind",
  props: {
    greet: String,
    name: String,
    channel: String,
    hack: String,
    channel2: String,
  },
};
</script>

<style>
</style>