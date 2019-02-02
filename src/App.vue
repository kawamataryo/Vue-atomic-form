<template>
  <div id="app">
    <form action="">
      <MyInput v-model="sampleForm.text" label="テキストエリア"></MyInput>
    </form>
  </div>
</template>

<script>
import MyInput from "@/components/MyInput";

export default {
  name: "app",
  components: {
    MyInput
  },
  data() {
    return {
      sampleForm: {
        text: "",
        radio: "",
        select: "",
        textarea: "",
        file: ""
      }
    };
  }
};
</script>

<style></style>
