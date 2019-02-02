<template>
  <button @click="click"><slot /></button>
</template>

<script>
export default {
  name: "MyBtn",
  methods: {
    click() {
      this.$emit("click");
    }
  }
};
</script>

<style scoped></style>
