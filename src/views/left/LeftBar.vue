<template>
  <div id="leftBar">
    <ul>
      <li
        v-for="(item, i) in barItems"
        :key="i"
        @click="handleClick(i)"
        :class="{ leftBarActive: i == currIndex }"
      >
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      barItems: ["发现音乐", "视频", "朋友", "直播", "私人FM"],
      currIndex: 0,
    };
  },
  methods: {
    handleClick(i) {
      this.currIndex = i;
    },
  },
};
</script>
<style lang='scss' scoped>
#leftBar {
  width: 200px;
  height: 100%;
  border-right: 1px solid #d6d6d6;
  ul {
    margin: 10px 10px 0 0;
  }
}
#leftBar li {
  margin: 2px 0 0 10px;
  display: block;
  border-radius: 2px;
  line-height: 30px;
  padding-left: 10px;
  font-size: var(--fontMid);
  &:hover {
    background: #f6f6f7;
  }
}
.leftBarActive {
  font-weight: bold;
  font-size: var(--fontMax) !important;
  background: #f6f6f7;
}
</style>