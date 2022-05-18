<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <!-- <div v-for="item in comments" :key="item.id"> -->
  <HelloWorld :comments="comments" />
  <!-- </div> -->
</template>

<script>
import HelloWorldVue from "./components/HelloWorld.vue";
import data from "./data.json";
export default {
  name: "App",
  components: {
    HelloWorld: HelloWorldVue,
  },
  data() {
    return {
      comments: data,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
