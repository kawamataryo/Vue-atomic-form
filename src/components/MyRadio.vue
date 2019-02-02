<template>
  <fieldset>
    <legend>{{ legend }}</legend>
    <template v-for="(option, index) in options">
      <label :key="index">
        <input
          type="radio"
          :name="name"
          :value="option.value"
          @change="updateValue"
        />{{ option.label }}
      </label>
    </template>
  </fieldset>
</template>

<script>
export default {
  name: "MyRadio",
  props: {
    value: { type: String, require: true },
    options: { type: Array, require: true },
    name: { type: String, require: true },
    legend: { type: String, require: true }
  },
  methods: {
    updateValue: function(e) {
      this.$emit("input", e.target.value);
    }
  }
};
</script>

<style scoped></style>
