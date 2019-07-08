<template>
  <div id="app">
    <img src="./assets/logo.png" />
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
    console.log(this.$store);
  },
  methods: {
    change() {
      this.$store.commit("change/name", "huang");
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
<style lang="less">
//less 文件不能像css在main.js中直接引入，需要在次处引入即可
@import "./assets/app.less";
</style>


