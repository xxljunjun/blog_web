<template>
  <div class="backTop">
    <div class="top updownbox" @click="backTop" v-if="btnFlag">
      <i class="el-icon-top"></i>
    </div>
    <div class="down updownbox" @click="backBottom">
      <i class="el-icon-bottom"></i>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      btnFlag: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.scrollToTop);
  },

  destroyed() {
    window.removeEventListener("scroll", this.scrollToTop);
  },
  methods: {
    backBottom(i) {
      let clientHeight =
        document.documentElement.clientHeight || document.body.clientHeight;
      let scrollHeight = document.documentElement.scrollHeight;
      let rollheight = scrollHeight - clientHeight; //超出窗口上界的值就是底部的scrolTop的值
      document.documentElement.scrollTop += 200;
      if (document.documentElement.scrollTop + 1 <= rollheight) {
        //之所以+1，可以打印这两个值的日志就知道了，下面+1也是同理
        var c = setTimeout(() => this.backBottom(i), 16); //调用setTimeout是为了“回到底部”这过程不是一瞬间
      } else {
        clearTimeout(c);
      }
    },
    backTop() {
      const that = this;
      let timer = setInterval(() => {
        let ispeed = Math.floor(-that.scrollTop / 5);
        document.documentElement.scrollTop = document.body.scrollTop =
          that.scrollTop + ispeed;
        if (that.scrollTop === 0) {
          clearInterval(timer);
        }
      }, 16);
    },

    scrollToTop() {
      const that = this;
      let scrollTop =
        window.pageYOffset ||
        document.documentElement.scrollTop ||
        document.body.scrollTop;
      that.scrollTop = scrollTop;
      if (that.scrollTop > 60) {
        that.btnFlag = true;
      } else {
        that.btnFlag = false;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.backTop {
  position: fixed;
  bottom: 20px;
  right: 20px;
  .updownbox {
    width: 30px;
    height: 30px;
    background: #fff;
    // border: 1px solid #000;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 5px;
    cursor: pointer;
    &:hover {
    }
  }
  .top {
    margin-bottom: 20px;
    .el-icon-top {
      font-weight: 600;
    }
    &:hover {
      .el-icon-top {
        color: red;
      }
    }
  }
  .down {
    .el-icon-bottom {
      font-weight: 600;
    }
    &:hover {
      .el-icon-bottom {
        color: red;
      }
    }
  }
}
</style>