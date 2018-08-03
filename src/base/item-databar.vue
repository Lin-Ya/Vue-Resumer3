<template>
  <div class="databar">
    <div class="content">
      <ItemInfo :msg="group.name"></ItemInfo>
      <div class="bar topbar" :style="{width:group.number+'%'}"></div>
      <div class="bar bottombar"></div>
    </div>
    <div class="num">
      <input contenteditable="true" v-model="group.number" maxlength="2">
      <span>%</span>
    </div>
  </div>
</template>

<script>
import "less/theme.less";
import ItemInfo from "base/item-info.vue";
export default {
  data() {
    return {
      source: null,
      default: {
        number: "80",
        name: {
          style: "brief",
          content: "java"
        }
      }
    };
  },
  props: {
    group: {
      type: Object
    }
  },
  components: {
    ItemInfo
  }
};
</script>

<style lang="less">
.databar {
  display: flex;
  align-items: flex-end;
  margin-top: 20px;
  justify-content: space-between;
  .content {
    position: relative;
    width: 240px;
    .bar {
      position: absolute;
      bottom: 0;
      left: 0;
      height: 2px;
      border-radius: 1px;
      background-color: #dfdfdf;
    }
    .topbar {
      z-index: 2;
      background-color: #38a1db;
      transition: all 0.3s;
    }
    .bottombar {
      width: 100%;
      z-index: 1;
    }
  }
  .num {
    opacity: 0;
    display: flex;
    input {
      width: 2em;
    }
  }
  &:hover .num {
    opacity: 1;
  }
}
</style>
