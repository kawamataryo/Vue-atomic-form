<template>
  <label><slot /></label>
</template>

<script>
export default {
  name: "MyLabel"
};
</script>

<style scoped lang="scss">
label {
  display: block;
  font-weight: bold;
  border-right: 5px solid #ccc;
  padding-right: 10px;
}
</style>
