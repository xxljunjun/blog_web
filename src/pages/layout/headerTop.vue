<template>
  <div class="header_box">
    <div class="header_left">
      <img src="@/assets/icons/home_1.png" alt="xxljunjun" title="导航栏" class="home" />
    </div>
    <div class="header_middle">
      {{ "军军 の" }}
      <span class="blue_box">博客园</span>
    </div>
    <div class="header_right">
      <img
        src="@/assets/icons/search.png"
        alt="xxljunjun"
        title="搜索"
        class="search"
      />
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  mounted() {},
  components: {},
  methods: {},
};
</script>
<style lang="scss" scoped>
.header_box {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 65px;
  background: #fff;
  width: 100%;
  position: fixed;
  top: 0;
  z-index: 10;
  .header_left {
    height: 65px;
    width: 65px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    &:hover {
      background: #eee;
    }
    .home {
      height: 20px;
      // width: 20px;
    }
  }
  .header_middle {
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 600;
    font-size: 20px;
    .blue_box {
      text-align: center;
      display: inline-block;
      height: 40px;
      width: 70px;
      background: red;
      border-radius: 5px;
      line-height: 40px;
      // padding:0  5px;
      margin-left: 5px;
      color: #fff;
    }
  }
  .header_right {
    height: 65px;
    width: 65px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    &:hover {
      background: #eee;
    }
    .search {
      height: 20px;
      //
    }
  }
}
</style>
