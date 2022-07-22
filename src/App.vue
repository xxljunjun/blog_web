<template>
  <div class="app_box">
    <headerTop />
    <div class="body_box">
      <bodyLeft />
      <div class="box_middle">
        <div class="language">
          <img src="@/assets/icons/pen.png" alt="" class="pen" />
          <ul class="lang">
            <li class="lang_txt">中文</li>
            <li>|</li>
            <li class="lang_txt">English</li>
            <li>|</li>
            <li class="lang_txt">日本语</li>
          </ul>
        </div>
        <router-view></router-view>
      </div>
      <bodyRight />
    </div>
  </div>
</template>
<script>
import headerTop from "@/pages/layout/headerTop.vue";
import bodyLeft from "@/pages/layout/bodyLeft.vue";
import bodyRight from "@/pages/layout/bodyRight.vue";
export default {
  name: "App",
  data() {
    return {};
  },
  mounted() {},
  components: {
    headerTop,
    bodyLeft,
    bodyRight,
  },
  methods: {},
};
</script>
<style lang="scss">
.app_box {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #666;
  .body_box {
    display: flex;
    width: 80%;
    align-items: flex-start;
    justify-content: space-between;
    padding: 32px 32px 0;
    margin-top: 64px;
    box-sizing: border-box;
    max-width: 1440px;
    overflow: visible;
    .box_middle {
      width: 100%;
      padding: 0 32px;
      .language {
        width: 100%;
        height: 48px;
        background: #fff;
        border-radius: 5px;
        margin-bottom: 32px;
        display: flex;
        align-items: center;
        .lang{
          display: flex;
          align-items: center;
         .lang_txt{
          color: red;
          cursor: pointer;
         }
          li{
             margin-right: 10px;
          }
        }
        .pen{
          margin-left: 20px;
          height: 20px;
          margin-right: 10px;
        }
      }
    }
  }
}
</style>
