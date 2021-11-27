<template>
  <div class="top-bar">
    <div class="top-bar-wrapper">
      <a href="#">
        <span class="logo"></span>
      </a>
      <div class="search-bar">
        <span>
          <input type="text" placeholder="大家正在搜:" class="search">
          <search-icon path="/search">
            <img slot="item-icon" src="@/assets/img/TopBar/search.png" alt="">
            <img slot="item-icon-active" src="@/assets/img/TopBar/search-fill.png" alt="">
          </search-icon>
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
          <top-bar-item path="/user">
            <img slot="item-icon" src="@/assets/img/TopBar/user.png" alt="">
            <img slot="item-icon-active" src="@/assets/img/TopBar/user-fill.png" alt="">
            <span slot="item-text">纸盒子_</span>
          </top-bar-item>
        </div>
        <div class="right-bar-right">
          <top-bar-item path="/email">
            <img slot="item-icon" src="@/assets/img/TopBar/mail.png" alt="">
            <img slot="item-icon-active" src="@/assets/img/TopBar/mail-fill.png" alt="">
          </top-bar-item>
          <top-bar-item path="/setting">
            <img slot="item-icon" src="@/assets/img/TopBar/setting.png" alt="">
            <img slot="item-icon-active" src="@/assets/img/TopBar/setting-fill.png" alt="">
          </top-bar-item>
          <div class="edit">
            <img src="@/assets/img/TopBar/edit-square.png" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TopBarItem from './TopBarItem.vue'
import SearchIcon from './SearchIcon.vue'

export default {
  name: 'TopBar',
  components: {
    TopBarItem,
    SearchIcon
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
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    display: block;
    margin-left: 120px;
    width: 110px;
    height: 48px;
    cursor: pointer;
    background: url('../../../assets/img/TopBar/WB_logo.png') no-repeat 0 40%;
  }

  .search-bar {
    flex: 1;
    display: block;
    position: relative;
  }

  .search {
    font-size: 12px;
    color: #808080;
    background-color: #F2F2F5;
    padding: 4px 33px 4px 10px;
    height: 20px;
    width: 425px;
    line-height: 20px;
    border: 1px solid #CCCCCC;
    border-radius: 0;
  }

  .search:focus {
    font-size: 12px;
    color: #808080;
    background-color: #F2F2F5;
    padding: 4px 33px 4px 10px;
    height: 20px;
    width: 425px;
    line-height: 20px;
    border: 1px solid #FA7D3C;
    border-radius: 0;
    outline: none;
  }

  .right-bar {
    display: flex;
    justify-content: flex-end;
    height: 26px;
  }

  .right-bar-left,
  .right-bar-right {
    font-size: 14px;
    display: flex;
  }

  .right-bar-left span{
    padding-right: 5px;
  }

  .right-bar-right {
    padding-left: 21px;
    margin-right: 90px;
    border-left: 1px solid #d9d9d9;
  }

  .edit {
    height: 26px;
    width: 24px;
    background: linear-gradient(to bottom, #fa7d3c 0%,#f56010 100%);
    text-align: center;
    border-radius: 2px;
    cursor: pointer;
  }

  .edit :hover{
    height: 26px;
    width: 24px;
    background: #f56010;
    text-align: center;
    border-radius: 2px;
    cursor: pointer;
  }

  .edit img{
    text-align: center;
    height: 20px;
    width: 20px;
    padding-top: 2px;
  }

  .edit:hover img{
    text-align: center;
    height: 20px;
    width: 20px;
    padding-top: 2px;
    padding-bottom: 4px;
    padding-left: 2px;
    padding-right: 2px;
  }
</style>