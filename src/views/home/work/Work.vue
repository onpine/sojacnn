<template>
  <div>
    <div class="work"><sunstance></sunstance></div>
  </div>
</template>

<script>
import Substance from "views/home/work/substance/Substance.vue";

export default {
  data() {
    return {
      msg: "",
    };
  },
  methods: {},
  components: {
    Substance,
    MainTabBar,
  },
};
</script>

<style scoped>
.work {
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
