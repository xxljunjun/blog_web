<template>
  <div class="pageBox">
    <div class="top_box">
      <div class="left_box">
        <img
          :src="require('@/assets/icons/' + imgsrc + '.png')"
          alt="xxljunjun"
          class="menu"
        />
        {{ title }}
      </div>
      <div class="right_box">
        <span>开启阅读模式</span>
        <img
          src="@/assets/icons/book.png"
          class="book"
        />
        </div>
    </div>
    <div class="content">
        <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    title: {
      type: String,
      default: "",
    },
    imgsrc: {
      type: String,
      default: "menu",
    },
  },
};
</script>

<style lang="scss" scoped>
@media screen and (max-width: 800px) {
  .top_box {
    height: 20px !important;
    padding: 0 4px !important;
    .left_box {
      .menu {
        height: 10px !important;
        margin-right: 4px !important;
      }
    }
}
}
.pageBox {
  background: #fff;
  border-radius: 5px;
  margin-bottom: 32px;
    .top_box {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 38px;
    padding: 0 10px;
    box-sizing: border-box;
    .left_box {
       display: flex;
    justify-content: center;
    align-items: center;
      .menu {
        height: 16px;
      }
    }
    .right_box {
      display: flex;
      align-items: center;
       cursor: pointer;
       color: #f30000;
      .book {
        height: 16px;
        margin-left: 5px;
       
      }
    }
  }
}
</style>