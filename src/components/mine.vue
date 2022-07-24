<template>
  <div class="mine">
    <img src="@/assets/avatar.jpg" alt="" class="avatar" />
    <div class="line"></div>
    <ul class="maessage">
      <li class="myName">junjunL</li>
      <li class="txt">你不解决问题，你就会成为问题</li>
      <li class="numbers">
        <img
          src="@/assets/icons/document.png"
          class="document icon"
          alt="xxljunjun"
        />

        <span class="num">15</span>
        <span class="bar">|</span>
        <img src="@/assets/icons/file.png" class="file icon" alt="xxljunjun" />

        <span class="num">18</span>
        <span class="bar">|</span>
        <img
          src="@/assets/icons/label.png"
          class="label icon"
          alt="xxljunjun"
        />
        <span class="num">24</span>
      </li>
      <li class="connect">
        <img
          src="@/assets/icons/github.png"
          class="github sociation"
          title="gitHub"
          @click="goToPage(1)"
        />
        <img
          src="@/assets/icons/email.png"
          class="email sociation"
          title="email"
          @click="goToPage(2)"
        />
        <img
          src="@/assets/icons/QQ.png"
          class="QQ sociation"
          title="QQ"
          @click="goToPage(3)"
        />
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "mine",
  data() {
    return {};
  },
  mounted() {},
  components: {},
  methods: {
    goToPage(val) {
      switch (val) {
        case 1:
          window.open('https://github.com/xxljunjun')
          break;
        case 2:
          break;
        case 3:
          break;
      }
    },
  },
};
</script>
<style lang="scss" scoped>
@media screen and (max-width: 800px) {
    .mine {
      flex-flow: row !important ;
      height: 80px !important;
      margin-bottom: 15px !important;
      .avatar {
        height: 60px !important;
        width: 60px !important;
        margin-left: 5px !important;
        padding-right: 10px !important;
        border-right: #ccc 2px dashed !important;
      }
      .line {
        display: none !important;
      }
      .maessage {
        margin-left: 20px !important;
      }
      .numbers {
        display: none !important;
      }
      .connect {
      .sociation {
        height: 12px !important;
      }
    }
    }
}
.mine {
  width: 100%;
  background: #fff;
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  margin-bottom: 32px;
  padding: 0 20px 20px;
  box-sizing: border-box;
  .avatar {
    height: 228px;
    width: 228px;
    margin: 20px 0;
    border-radius: 5px;
  }
  .line {
    height: 0;
    width: 100%;
    border-bottom: #ccc 4px dashed;
  }
  .maessage {
    display: flex;
    flex-direction: column;
    align-items: center;
    .myName {
      font-weight: 600;
      font-size: 20px;
      text-shadow: 18px 18px #eee;
      margin-bottom: 15px;
    }
    .txt {
       margin-bottom: 15px;
    }
    .numbers {
      margin-top: 0;
       margin-bottom: 15px;
      .icon {
        height: 20px;
        margin-right: 5px;
      }
      .bar {
        display: inline-block;
        margin: 0 5px;
      }
      .num {
        margin-right: 5px;
      }
    }
    .connect {
      margin-top: 0;
      display: flex;
      align-items: center;
      justify-content: center;

      .github {
        margin-right: 20px;
      }
      .email {
        margin-right: 20px;
      }
      .QQ {
      }
      .sociation {
        height: 25px;
        cursor: pointer;
      }
    }
  }
}
</style>
