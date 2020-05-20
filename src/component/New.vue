<template>
  <div>
    <h2>New</h2>
    <button @click="counter++">click</button>
    <p>{{ counter }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0
    };
  },
  destroyed() {
      console.log("destroyed");
  },
  deactivated() {
      console.log("deactived")
  },
  activated() {
      console.log("activated")
  },
};
</script>

<style scoped></style>
