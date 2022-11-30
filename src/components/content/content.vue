<template>
  <div>
    <Row type="flex" justify="space-between" class="code-row-bg">
      <Col span="6">
        <div class="content">
          <div class="login">
            <Avatar icon="ios-person" size="large" id="avatar" />
            <p>
              <span><a href="javascript:0;">未登录</a></span>
              <Icon type="md-arrow-dropright" />
            </p>
          </div>

          <Menu active-name="1" style="width: none" id="menu">
            <MenuItem name="1" id="menu1" @click.native="comName = 'MyFind'">
              <Icon type="ios-musical-notes" />
              发现音乐
            </MenuItem>
            <MenuItem name="2" @click.native="comName = 'MyPodcast'">
              <Icon type="md-headset" />
              播客
            </MenuItem>
            <MenuItem name="3" @click.native="comName = 'MyPrivate'">
              <Icon type="ios-cash" />
              私人FM
            </MenuItem>
            <MenuItem name="4" @click.native="comName = 'MyVideo'">
              <Icon type="md-play" />
              视频
            </MenuItem>
            <MenuItem name="5" @click.native="comName = 'MyFollow'">
              <Icon type="md-contacts" />
              关注
            </MenuItem>
            <MenuGroup title="我的音乐">
              <MenuItem name="6">
                <Icon type="md-heart" />
                我喜欢的音乐
              </MenuItem>
              <MenuItem name="7">
                <Icon type="md-arrow-dropright-circle" />
                iTunes音乐
              </MenuItem>
              <MenuItem name="8">
                <Icon type="md-leaf" />
                下载管理
              </MenuItem>
              <MenuItem name="9">
                <Icon type="ios-flag" />
                最近播放
              </MenuItem>
            </MenuGroup>
          </Menu>
        </div>
      </Col>
      <Col span="18">
        <component :is="comName"></component>
      </Col>
    </Row>
  </div>
</template>

<script>
import MyFind from "@/views/MyFind";
import MyPodcast from "@/views/MyPodcast";
import MyPrivate from '@/views/MyPrivate';
import MyVideo from "@/views/MyVideo";
import MyFollow from '@/views/MyFollow';
export default {
  data() {
    return {
      comName: "MyFind",
    };
  },
  methods: {
 
  },
  components: {
    MyFind,
    MyPodcast,
    MyPrivate,
    MyVideo,
    MyFollow,
  },
};
</script>

<style scoped>
@import "./content.css";
</style>
