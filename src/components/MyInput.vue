<template>
  <label>
    {{ label }}
    <input
      type="text"
      :name="name"
      :value="value"
      :placeholder="placeholder"
      @input="updateValue"
    />
  </label>
</template>

<script>
export default {
  name: "MyInput",
  props: {
    value: { type: String, require: true },
    name: { type: String, require: true },
    label: { type: String, require: true },
    placeholder: { type: String, require: false }
  },
  methods: {
    updateValue: function(e) {
      this.$emit("input", e.target.value);
    }
  }
};
</script>

<style scoped lang="stylus">

</style>
