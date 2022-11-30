<template>
  <Col span="8" id="title-main">
    <li @click="comName = 'MyFind'">个性推荐</li>
    <li>歌单</li>
    <li>排行榜</li>
    <li>歌手</li>
    <li>最新音乐</li>
    
  </Col>
  
</template>

<script>
import MyFind from "../views/MyFind.vue";
export default {
  data() {
    return {
      comName: "MyFind",
    };
  },
  components: {
    MyFind,
   
  },
};
</script>

<style scoped>
 @import "./headStyle.css";
</style>