<template>
  <div class="top-bar">
    <!-- <span class="left">left</span>
    <span class="middle">middle</span>
    <span class="right">right</span> -->
    <div class="top-bar-wrapper">
      <a href="#">
        <span class="logo"></span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TopBar'
}
</script>

<style scoped>
  .top-bar {
    position: fixed;
    display: flex;
    align-items: center;

    height: 48px;
    width: 100%;
    /* 限制最大宽度 */
    /* max-width: 800px; */
    top: 0;
    /* 水平居中 */
    left: 50%;
    transform: translateX(-50%);

    background-color: #fff;
    border-top: 2px solid #FA7D3C;

    box-shadow: 0 2px 4px rgba(0, 0, 0, .2);
  }

  .top-bar-wrapper{
    position: relative;
    left: 50%;
    transform: translateX(-50%);
  }

  .logo{
    display: block;
    margin-left: 50px;
    width: 140px;
    height: 48px;
    cursor: pointer;
    background: url('../../assets/img/TopBar/WB_logo.png') no-repeat 0 40%;
  }

  .left,
  .middle,
  .right {
    height: 44px;
    text-align: center;
    line-height: 44px;
    border: 1px solid black;
  }

  .left {
    width: 150px;
  }

  .middle {
    height: 26px;
    line-height: 26px;
    flex: 1;
    margin: 6px 10px;
    border-radius: 5px;
  }

  .right {
    width: 150px;
  }
</style>