<template>
  <div class="main-container">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <div class="container">
      <div class="child1">test1</div>
      <div class="child2">test2</div>
      <div class="child3 none">test3</div>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/abstract/_functions.scss";
@import "@/assets/scss/abstract/_mixins.scss";
@import "@/assets/scss/abstract/_variables.scss";
.main-container {
  @include set-flex(column, center, center);
  text-align: center;
  padding-top: 6rem;
  .container {
    .child1 {
      @include set-font($font-base, 700, $red2);
    }
    .child3 {
      &.none {
        display: none;
      }
    }
  }
}
</style>
