<template>
  <div class="top-bar">
    <span class="left">left</span>
    <span class="middle">middle</span>
    <span class="right">right</span>
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

    height: 44px;
    width: 100%;
    /* 限制最大宽度 */
    /* max-width: 800px; */
    top: 0;
    /* 水平居中 */
    left: 50%;
    transform: translateX(-50%);

    background-color: #f6f6f6;
    border-top: 1px solid #ccc;
    border-bottom: 1px solid #ccc;

    box-shadow: 0 2px 4px rgba(0, 0, 0, .2);
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