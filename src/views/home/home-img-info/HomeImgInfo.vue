<template>
<div>
    <main-tab-bar></main-tab-bar>
  <div class="home-img-info">
    <current-location></current-location>
    <navigation></navigation>
    <corresponding-content></corresponding-content>
  </div>
</div>
</template>

<script>
import CurrentLocation from "views/home/home-img-info/header/current-location/CurrentLocation.vue";
import Navigation from "views/home/home-img-info/bottom/navigation/Navigation.vue";
import CorrespondingContent from "views/home/home-img-info/bottom/correspondingcontent/CorrespondingContent.vue";
import MainTabBar from "components/content/mainTabbar/MainTabBar.vue";

export default {
  data() {
    return {
      msg: "",
    };
  },
  methods: {},
  components: {
    CurrentLocation,
    Navigation,
    CorrespondingContent,
    MainTabBar,
  },
};
</script>

<style scoped>
.home-img-info {
  width: 1200px;
  min-width: 1200px;
  height: 2000px;
  /* background: yellowgreen; */
  position: absolute;
  left: 0;
  right: 0;
  margin: 0 auto;
  top: 181px;
}
</style>
