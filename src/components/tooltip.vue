<template>
  <div class="hello">
    <h1>ToolTip</h1>

    <div class="container">
      <label class="tooltip_label">阈值</label>
      <input class="tooltip_input" type="text" v-model="threshold">
      <div class="tooltip_container">
        <div class="tooltip_img">
          <img src="@/assets/tooltip.png" width="20" height="20" alt="">
        </div>
        <div class="tooltip">
          <img class="triangle" src="@/assets/triangle.png" width="12" height="12" alt="">
          <span>注: 单位为秒, 目标范围最小为80, 最大为200</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ToolTip",
  data() {
    return {
      threshold: ''
    }
  }
}
</script>

<style scoped lang="scss">
.container {
  position: relative;
}
.tooltip_label {
  font-size: 14px;
  color: #909399;
}
.tooltip_input {
  margin-left: 20px;
  width: 200px;
  height: 20px;
  line-height: 20px;
  outline-offset: none;
  outline: none;
  border: none;
  font-size: 12px;
  padding-left: 17px;
  color: #303133;
  border: 1px solid #dbdce7
}
.tooltip_input:hover {
  outline-offset: none;
  outline: none;
  border: 1px solid #909399;
  cursor: text;
}
.tooltip_input:active {
  outline-offset: none;
  outline: none;
  border: 1px solid #909399;
}

.tooltip_container {
  display: inline-flex;
  flex-direction: row;
  justify-content: flex-start;
  margin-left:10px;
  width: 400px;
  .tooltip_img {
    width: 20px;
    height: 20px;
  }
  .tooltip {
    display: none;
    width: 260px;
    height: 26px;
    line-height: 20px;
    border-radius: 4px;
    background: #303133;
    color: #ffffff;
    font-size: 12px;
    margin-left: 20px;
  }
  &:hover {
    .tooltip {
      display: block;
    }
  }
}
.triangle {
  margin: 5px 0 0 -9px
}
</style>
