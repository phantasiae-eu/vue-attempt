<template>
  <div class="about">
    <h1>This is an about page</h1>
    <p>{{bkg}}</p>
    <vue-qr :bgSrc="bkg" :logoSrc="src2" text="Hello world!" :size="400"></vue-qr>
    <vue-qr text="Hello world!" :callback="test" qid="testid"></vue-qr>
    <img :src="bkg" :alt="bkg">
  </div>
</template>


<script>
import Vue from "vue";
import VueQr from "vue-qr";
console.log(VueQr);
const backgroundSource = "src/assets/logo.png";

new Vue({
  components: { VueQr }
});

export default {
  components: {
    VueQr
  },
  data: function() {
    return {
      // bkg: require("../assets/logo.png")
      bkg: require("../assets/logo.png"),
      src2: require("../assets/superstar.gif")
    };
  },
  methods: {
    test(dataUrl, id) {
      // eslint-disable-next-line
      console.log(url, id);
    }
  }
};
</script>