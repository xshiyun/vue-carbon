<template>
  <div class="header-bar">
    <div class="left">
      <slot name="left"></slot>
    </div>
    <div class="center">
      <slot></slot>
    </div>
    <div class="right">
      <slot name="right"></slot>
    </div>
  </div>
</template>

<style lang="less">
@import "../utils/_vars.less";
@import "../utils/_mixins.less";
.header-bar {
  display: flex;
  align-self: flex-start;
  justify-content: flex-start;
  align-items: center;
  color: #FFF;
  background-color: @barcolor;
  font-size: 20px;
  height: @header-height;
  width: 100%;
  .flex-shrink(0);
  > .left,
  > .right{
    .flex-shrink(0);
    display: flex;
    justify-content: flex-start;
    align-items: center;
  }
  > .center{
    flex: 1;
    line-height: @header-height;
    overflow: hidden;
    text-overflow: ellipsis;
    padding-left: 16px;
    padding-right: 16px;
    white-space: nowrap;
  }
  
  .button {
    font-size: 18px;
    background: none;
    height: 56px;
    line-height: 56px;
    color: #FFF;
    .ripple-ink{
      color: rgba(255, 255, 255, .3);
    }
  }

  .icon-button {
    background: none;
    width: 56px;
    height: 56px;
    color: #FFF;
    .ripple-ink{
      color: rgba(255, 255, 255, .3);
    }
  }
}
</style>
