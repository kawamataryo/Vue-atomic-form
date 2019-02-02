<template>
  <div id="app">
    <form action="">
      <MyLabel>InputText</MyLabel>
      <MyInput
        v-model="sampleForm.text"
        placeholder="サンプル"
        name="sample-input"
        type="text"
      ></MyInput>
      <MyLabel>TextArea</MyLabel>
      <MyTextarea
        v-model="sampleForm.textarea"
        placeholder="サンプル"
        name="sample-textarea"
        :rows="10"
        :cols="50"
      ></MyTextarea>
      <MyLabel>RadioButton</MyLabel>
      <MyRadio
        v-model="sampleForm.radio"
        name="sample-radio"
        :options="options"
      ></MyRadio>
      <MyLabel>Checkbox</MyLabel>
      <MyCheckbox
        v-model="sampleForm.checkbox"
        name="sample-checkbox"
        :options="options"
      ></MyCheckbox>
      <MyLabel>Select</MyLabel>
      <MySelect
        v-model="sampleForm.select"
        name="sample-select"
        :options="options"
      ></MySelect>
      <MyBtn @click="sendForm">send</MyBtn>
    </form>
  </div>
</template>

<script>
import MyInput from "./components/MyInput";
import MyTextarea from "./components/MyTextarea";
import MyRadio from "./components/MyRadio";
import MyCheckbox from "./components/MyCheckbox";
import MySelect from "./components/MySelect";
import MyBtn from "./components/MyBtn";
import MyLabel from "./components/MyLabel";

export default {
  name: "app",
  components: {
    MyTextarea,
    MyInput,
    MyRadio,
    MyCheckbox,
    MySelect,
    MyBtn,
    MyLabel
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
  },
  methods: {
    sendForm() {
      // formデータの送信処理
    }
  }
};
</script>

<style></style>
