<template>
  <div id="app" class="wrapper">
    <router-view />
    <div class="mec">

    <HelloWorld />
    </div>

  </div>
</template>

<script>
import MainTabBar from "components/content/mainTabbar/MainTabBar.vue";
import HelloWorld from './common/HelloWorld.vue'

export default {
  name: "app",
  data() {
    return {
      
    }
  },
  components: {
    MainTabBar,
    // HelloWorld,
  },
};
</script>

<style>
@import "assets/css/base.css";
/* .mec{
  position: absolute;
  bottom: -3000px;
  left: 400px;
} */
</style>
