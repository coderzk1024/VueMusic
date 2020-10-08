<template>
  <div class="navBar">
    <div class="headerLeft">
      <img src="@/assets/img/music.svg" class="headerIcon" />
      <span class="title">网抑云音乐</span>
      <div class="titleRoute"><img src="@/assets/img/back.svg" /></div>
      <div class="titleRoute"><img src="@/assets/img/forword.svg" /></div>
      <div class="serach">
        <img src="@/assets/img/search.svg" />
        <input type="text" placeholder="搜索" />
      </div>
    </div>
    <div class="headerRight">
      <div class="userLogo">
        <el-image :src="userLogo">
          <div slot="error" class="image-slot iconBackground">
            <img class="iconHolder" src="@/assets/img/user.svg" />
          </div>
        </el-image>
      </div>
      <span>未登录<i class="el-icon-caret-bottom"></i></span>
      <span>开通VIP</span>
      <i class="el-icon-setting iconClass"></i>
      <img src="@/assets/img/skin.svg" class="iconClass" />
      <i class="el-icon-message iconClass" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userLogo: "",
    };
  },
};
</script>
<style lang='scss' scoped>
.navBar {
  width: 100%;
  height: 60px;
  background: #ec4141;
  color: #fff;
  display: flex;
  justify-content: space-between;
}
.headerLeft {
  display: flex;
  align-items: center;
  .headerIcon {
    width: 30px;
  }
  .title {
    font-size: var(--fontMax);
    margin-right: 110px;
  }
  .titleRoute {
    margin-right: 10px;
    border-radius: 50%;
    background: #d93b3b;
    // height: 18px;
    // border: 1px solid black;
    height: 25px;
    width: 25px;
    text-align: center;
    line-height: 25px;
    cursor: pointer;
  }
  .titleRoute > img {
    height: 10px;
  }
  .serach {
    width: 160px;
    height: 30px;
    background: #d93b3b;
    border-radius: 15px;
    display: flex;
    align-items: center;
  }
  .serach > img {
    margin-left: 10px;
    height: 20px;
  }
  .serach > input {
    background-color: transparent;
    outline: none;
    border: none;
    width: 120px;
    font-size: var(--fontMini);
    color: #fff;
    // border-style: none;
    // text-shadow: none;
    // -webkit-appearance: none;
    // -webkit-user-select: text;
    // box-shadow: none;
  }
  .serach > input::placeholder {
    font-size: var(--fontMini);
    color: #c8c8c8;
  }
}
.headerRight {
  // flex: 1;
  width: 400px;
  display: flex;
  align-items: center;
  .userLogo {
    height: 24px;
  }
}
.headerRight > span {
  margin-left: 10px;
  font-size: var(--fontMini);
  cursor: pointer;
}
.iconBackground {
  height: 25px;
  width: 25px;
}
.iconHolder {
  height: 24px;
  background-color: #e0e0e0;
  border-radius: 50%;
}
.iconClass {
  margin-left: 10px;
  height: 16px;
  font-size: 16px;
  cursor: pointer;
}
</style>