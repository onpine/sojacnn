<template>
  <div>
    <main-tab-bar></main-tab-bar>
    <div class="gsosp">
      <el-container>
        <el-header>
          <div class="current-location">
            <h2>科普概况</h2>
            <p>
              <a href="/gsosp">科普概况</a>
              <span>/</span>
              当前位置: <a href="/home">首页</a>
            </p>
          </div>
        </el-header>
        <el-container>
          <el-aside width="200px">
            <el-row class="tac">
              <el-col :span="12">
                <el-menu
                  default-active="2"
                  class="el-menu-vertical-demo"
                  text-color="#fff"
                  active-text-color="#409EFF"
                >
                  <el-menu-item
                    @click="getPath(item.id)"
                    v-for="item in MenuList"
                    :key="item.id"
                  >
                    <i class="el-icon-menu"></i>
                    <span slot="title">{{ item.categoryName }}</span>
                  </el-menu-item>
                </el-menu>
              </el-col>
            </el-row>
          </el-aside>
          <el-main>
            <router-view></router-view>
          </el-main>
        </el-container>
      </el-container>
    </div>
  </div>
</template>

<script>
import { findCategoryByContypeId } from "@/api/index";

import MainTabBar from "components/content/mainTabbar/MainTabBar.vue";

export default {
  data() {
    return {
      MenuList: [],
    };
  },
  mounted() {
    this.initMenu();
  },
  components: {
    MainTabBar,
  },
  methods: {
    async initMenu() {
      let result = await findCategoryByContypeId({ contypeId: 2 });
      this.MenuList = [...result.data.data.items];
      console.log(this.MenuList);
    },
    menuClick() {},
    getPath(id) {
      // if(id == 1){
      //   this.$router.push("/gsnavigation")
      // }
      switch (id) {
        case 1:
          this.$router.push("/index1");
          break;
        case 2:
          this.$router.push("/index2");
          break;
        // case 3:
        //   this.$router.push('/gsnavigation')
        //   break;
        // case 4:
        //   this.$router.push('/gsnavigation')
        //   break;
        // case 5:
        //   this.$router.push('/gsnavigation')
        //   break;

        default:
          break;
      }
    },
  },
};
</script>


<style>
.gsosp {
  width: 1200px;
  min-width: 1200px;
  height: 2000px;
  /* background: yellowgreen; */
  position: absolute;
  left: 0px;
  right: 0px;
  margin: 0 auto;
  top: 181px;
}
.el-col-12 {
    width: 80%;
}
.current-location {
  width: 1200px;
  height: 50px;
  background: rgb(255, 255, 255);
  margin-top: 10px;
  line-height: 50px;
}
.current-location h2{
  display: inline-block;
  color: #1675e2;
}
.current-location p{
  float: right;
}
.current-location p a{
  float: right;
}
.current-location p a:hover{
  color: #1675e2;
}
.current-location span{
  float: right;
}
</style>
