<template>
  <div id="app">
    <div class="container">
      <div class="d-flex align-items-center justify-content-md-end">
        <div class="col-md-8 col-xs-12">
          <div id="nav">
            <router-link to="/">Home</router-link> |
            <router-link to="/about">About</router-link> |
            <router-link to="/git">GitHub</router-link>
          </div>
        </div>
        <div id="lang-bar" class="col-xs-12 col-md-2">
          <langComponent />
        </div>
      </div>
      <div class="row">
        <div class="col">
          <router-view />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import LanguageBarVue from "./components/LanguageBar.vue";
export default {
  name: "App",
  components: {
    langComponent: LanguageBarVue,
  },
};
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

body {
  background: rgb(249, 252, 248);
  // position: relative;
}
#lang-bar {
  // width: 100%;
  // height: 50%;
  // left: %;
  // bottom: 50%;
  // min-width: 100%;
  padding: 20px;
  // z-index: -1;
}
#navbar-col {
}
</style>
