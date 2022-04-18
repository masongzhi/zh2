<template>
  <input type="text" v-model="value" />

  <div class="zh2">二简字: {{ value }}</div>

  <div class="desc">
    <div>字体下载: <a href="/zh2.ttf">二简字.ttf</a></div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "App",
  setup() {
    const value = ref<string>(
      "雪夜里饮酒，见蝴蝶起舞，樱花、石榴、荔枝，朦胧又愉悦的腾飞着 —— 《赠别野花 卷二》"
    );

    return {
      value,
    };
  },
});
</script>

<style lang="scss">
@import "~@/assets/normalize.scss";

@font-face {
  font-family: zh2;
  src: url("../public/zh2.ttf");
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

  input {
    width: 800px;
  }

  .zh2 {
    margin-top: 10px;
    font-family: zh2;
    font-weight: bold;
  }

  .desc {
    margin-top: 50px;
  }
}
</style>
