<template>
  <div class="tab-bar-item" @mouseover="onHover" @mouseout="notHover">
    <span v-if="isActive || isHovering"><slot name="item-icon-active"></slot></span>
    <span v-else><slot name="item-icon"></slot></span>
    <span :class="{active:isActive}"><slot name="item-text"></slot></span>
  </div>
</template>

<script>
export default {
  name: 'SearchIcon',
  props: {
    path: String
  },
  data() {
    return {
      isHovering: false
    }
  },
  computed: {
    isActive() {
      return this.$route.path == this.path
    }
  },
  methods: {
    onHover() {
      this.isHovering = true;
    },
    notHover() {
      this.isHovering = false;
    }
  }
}
</script>

<style scoped>
.tab-bar-item{
  position: absolute;
  top: 4px;
  left: 440px;
  white-space: nowrap;
  height: 30px;
  font-size: 14px;
  margin-right: 20px;
  cursor: pointer;
}

.tab-bar-item:hover{
  height: 30px;
  font-size: 14px;
  margin-right: 20px;
  color: #FA7D3C;
  cursor: pointer;
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