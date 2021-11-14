<template>
  <div class="top-bar">
    <div class="top-bar-wrapper">
      <a href="#">
        <span class="logo"></span>
      </a>
      <div class="search-bar">
        <span>
          <input type="text" placeholder="大家正在搜:" class="search">
          <a href="#" title="搜索" class="search-icon"></a>
        </span>
      </div>
      <div class="right-bar">
        <div class="right-bar-left">
          <top-bar-item path="/home">
            <img slot="item-icon" src="@/assets/img/TopBar/home.png" alt="">
            <img slot="item-icon-active" src="@/assets/img/TopBar/home-fill.png" alt="">
            <span slot="item-text">首页</span>
          </top-bar-item>
          <top-bar-item path="/video">
            <img slot="item-icon" src="@/assets/img/TopBar/video.png" alt="">
            <img slot="item-icon-active" src="@/assets/img/TopBar/video-fill.png" alt="">
            <span slot="item-text">视频</span>
          </top-bar-item>
          <top-bar-item path="/discover">
            <img slot="item-icon" src="@/assets/img/TopBar/compass.png" alt="">
            <img slot="item-icon-active" src="@/assets/img/TopBar/compass-fill.png" alt="">
            <span slot="item-text">发现</span>
          </top-bar-item>
          <top-bar-item path="/game">
            <img slot="item-icon" src="@/assets/img/TopBar/smile.png" alt="">
            <img slot="item-icon-active" src="@/assets/img/TopBar/smile-fill.png" alt="">
            <span slot="item-text">游戏</span>
          </top-bar-item>
        </div>
        <div class="right-bar-right">
          <top-bar-item path="/email">
            <img slot="item-icon" src="@/assets/img/TopBar/mail.png" alt="">
            <img slot="item-icon-active" src="@/assets/img/TopBar/mail-fill.png" alt="">
          </top-bar-item>
          <top-bar-item path="/email">
            <img slot="item-icon" src="@/assets/img/TopBar/setting.png" alt="">
            <img slot="item-icon-active" src="@/assets/img/TopBar/setting-fill.png" alt="">
          </top-bar-item>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TopBarItem from './TopBarItem.vue'

export default {
  name: 'TopBar',
  components: {
    TopBarItem
  },
  data() {
    return {
    }
  },
  methods: {
  }
}
</script>

<style scoped>
  .top-bar {
    position: fixed;
    display: flex;
    justify-content: center;

    height: 48px;
    width: 100%;
    /* 限制最大宽度 */
    /* max-width: 800px; */
    top: 0;
    /* 水平居中 */
    /* left: 50%;
    transform: translateX(-50%); */

    background-color: #fff;
    border-top: 2px solid #FA7D3C;

    box-shadow: 0 2px 4px rgba(0, 0, 0, .2);
  }

  .top-bar-wrapper {
    position: relative;
    display: flex;
    align-items: center;
  }

  .logo {
    display: block;
    margin-left: 50px;
    width: 140px;
    height: 48px;
    cursor: pointer;
    background: url('../../../assets/img/TopBar/WB_logo.png') no-repeat 0 40%;
  }

  .search-bar {
    display: block;
  }

  .search {
    font-size: 12px;
    color: #808080;
    background-color: #F2F2F5;
    padding: 4px 33px 4px 10px;
    height: 20px;
    line-height: 20px;
    border: 1px solid #CCCCCC;
    border-radius: 0;
  }

  .right-bar {
    display: flex;
    justify-content: flex-end;
    height: 26px;
    width: 580px;
  }

  .right-bar-left,
  .right-bar-right {
    font-size: 14px;
    display: flex;
  }

  .right-bar-left span{
    padding-right: 5px;
  }

  .right-bar-right{
    border-left: 1px solid #d9d9d9;
  }
</style>