<template>
  <div>
    <div class="container">
      <div class="title">
        <Row id="row" type="flex" justify="space-around" class="code-row-bg">
          <Col span="4"></Col>
              <MyHead></MyHead>
          <!-- title右边 -->
          <Col span="9" id="cor-right">
            <Input
              prefix="ios-search"
              placeholder="搜索"
              style="width: auto"
              id="ipt"
            />
            <div class="icon">
              <Icon type="md-settings" />
              <Icon type="md-mail" />
              <Icon type="ios-shirt" />
              <Icon type="ios-photos" />
            </div>
          </Col>
        </Row>
      </div>
      
      <tent></tent>
   
        
      
    </div>
  </div>
  
</template>

<script>
import tent from "./components/content/content.vue";
import middle from "./components/middle/middle.vue";
import MyHead from "./head/MyHead";

export default {
  components: {
    tent,
    middle,
    MyHead,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style>
li {
  list-style: none;
}
.container {
  margin: auto;
  width: 1030px;
  height: 675px;
  margin-top: 50px;
}
#row {
  height: 50px;
  background-color: #2b2b2b;
}

/* #title-main {
  display: flex;
  justify-content: space-around;
  align-items: center;
  font-size: 14px;
}
#title-main li {
  cursor: pointer;
  color: #6e6e6e;
}
#title-main li:hover {
  color: #fff;
} */
#ipt .ivu-input {
  outline: none !important;
  background-color: #4b4b4b;
  border: none;
  color: #9e9e9e;
  border-radius: 20px;
  margin-right: 10px;
}
#ipt .ivu-input-inner-container {
  margin-right: 20px;
}
#cor-right {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}
.icon i {
  margin-right: 20px;
  font-size: 18px;
  color: #6e6e6e;
  cursor: pointer;
}
</style>