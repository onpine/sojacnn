<template>
<div>
    <main-tab-bar></main-tab-bar>

  <div class="circulars">
    <sunstance></sunstance>
  </div>
</div>
</template>

<script>
import Substance from 'views/home/circulars/substance/Substance.vue'
import MainTabBar from "components/content/mainTabbar/MainTabBar.vue";

export default {
  data() {
    return {
      msg: "",
    };
  },
  methods: {},
  components:{
    Substance,
    MainTabBar
  }
};
</script>

<style scoped>
.circulars {
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
