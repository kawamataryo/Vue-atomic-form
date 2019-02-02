<template>
  <div id="app">
    <form action="">
      <MyInput
        v-model="sampleForm.text"
        legend="インプトテキスト"
        placeholder="サンプル"
        name="sample-input"
        type="text"
      ></MyInput>
      <MyTextarea
        v-model="sampleForm.textarea"
        legend="テキストエリア"
        placeholder="サンプル"
        name="sample-textarea"
        :rows="10"
        :cols="50"
      ></MyTextarea>
      <MyRadio
        v-model="sampleForm.radio"
        legend="ラジオボタン"
        name="sample-radio"
        :options="options"
      ></MyRadio>
      <MyCheckbox
        v-model="sampleForm.checkbox"
        legend="チェックボックス"
        name="sample-checkbox"
        :options="options"
      ></MyCheckbox>
      <MySelect
        v-model="sampleForm.select"
        name="sample-select"
        legend="セレクトボックス"
        :options="options"
      ></MySelect>
    </form>
  </div>
</template>

<script>
import MyInput from "./components/MyInput";
import MyTextarea from "./components/MyTextarea";
import MyRadio from "./components/MyRadio";
import MyCheckbox from "./components/MyCheckbox";
import MySelect from "./components/MySelect";

export default {
  name: "app",
  components: {
    MyTextarea,
    MyInput,
    MyRadio,
    MyCheckbox,
    MySelect
  },
  data() {
    return {
      sampleForm: {
        text: "",
        radio: "",
        select: "",
        textarea: "",
        checkbox: []
      },
      options: [
        {
          label: "fizz",
          value: "3"
        },
        {
          label: "buzz",
          value: "5"
        },
        {
          label: "fizzBuzz",
          value: "15"
        }
      ]
    };
  }
};
</script>

<style></style>
