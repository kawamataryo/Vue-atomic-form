<template>
  <div id="app">
    <form action="">
      <MyInputText v-model="sampleForm.text" label="テキスト"></MyInputText>
    </form>
  </div>
</template>

<script>
import MyInputText from "@/components/MyInputText";

export default {
  name: "app",
  components: {
    MyInputText
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
