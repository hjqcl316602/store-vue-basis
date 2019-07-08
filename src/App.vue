<template>
  <div id="app">
    <div class="main"></div>
    <span class="vc-text--clamp">
      {{ $store.state.basis.name }}
    </span>
    <button @click="change">change</button>
    <router-view />
  </div>
</template>

<script>
export default {
  name: "App",
  mounted() {
    console.log(this.config);
  },
  methods: {
    change() {
      this.$store.commit("change/name", "huang");
    }
  }
};
</script>

<style>
</style>
<style lang="less">
//less 文件不能像css在main.js中直接引入，需要在次处引入即可
@import "./css/basis/index.less";
</style>


