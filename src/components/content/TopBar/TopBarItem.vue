<template>
  <div class="tab-bar-item">
    <span v-if="isActive"><slot name="item-icon-active"></slot></span>
    <span v-else><slot name="item-icon"></slot></span>
    <span :class="{active:isActive}"><slot name="item-text"></slot></span>
  </div>
</template>

<script>
export default {
  name: 'TopBarItem',
  props: {
    path: String
  },
  computed: {
    isActive() {
      return this.$route.path == this.path
    }
  }
}
</script>

<style scoped>
.tab-bar-item{
  flex: 1;
  text-align: center;
  height: 30px;
  font-size: 14px;
  padding-right: 20px;
}

.tab-bar-item img{
  height: 24px;
  width: 24px;
  margin-bottom: 2px;
  margin-right: 3px;
  vertical-align: middle;
}

.active{
  color: #FA7D3C;
}

</style>