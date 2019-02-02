<template>
  <fieldset>
    <legend>{{ legend }}</legend>
    <textarea
      :name="name"
      :value="value"
      :placeholder="placeholder"
      :rows="rows"
      :cols="cols"
      @input="updateValue"
    ></textarea>
  </fieldset>
</template>

<script>
export default {
  name: "MyTextarea",
  props: {
    value: { type: String, require: true },
    name: { type: String, require: true },
    legend: { type: String, require: true },
    placeholder: { type: String, require: false },
    rows: { type: Number, require: false },
    cols: { type: Number, require: false }
  },
  methods: {
    updateValue: function(e) {
      this.$emit("input", e.target.value);
    }
  }
};
</script>

<style scoped></style>
