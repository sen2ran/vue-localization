<template>
  <div id="app">
    <div>
      <a @click="setLocalizationFn('en')">
        <flag iso="us" />
      </a>
      <br>
      <a @click="setLocalizationFn('ru')">
        <flag iso="ru" />
      </a>
      <br>
      <a @click="setLocalizationFn('lk')">
        <flag iso="lk" />
      </a>
    </div>
    <div id="nav">
      <router-link to="/">Home</router-link>|
      <router-link to="/about">About</router-link>
    </div>
    <router-view />
  </div>
</template>


<script>
export default {
  methods: {
    setLocalizationFn(val) {
     this.$i18n.locale = val
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
