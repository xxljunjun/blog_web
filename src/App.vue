<template>
  <div class="app_box">
    <headerTop />
    <div class="body_box">
      <bodyLeft />
      <div class="box_middle">
        <!-- <div class="language">
          <img src="@/assets/icons/pen.png" alt="" class="pen" />
          <ul class="lang">
            <li class="lang_txt">中文</li>
            <li>|</li>
            <li class="lang_txt">English</li>
            <li>|</li>
            <li class="lang_txt">日本语</li>
          </ul>
        </div> -->
        <router-view></router-view>
      </div>
      <bodyRight />
    </div>
    <backTop/>
  </div>
</template>
<script>
/*  
  小帅哥： https://unpkg.com/live2d-widget-model-chitose@1.0.5/assets/chitose.model.json
		萌娘：https://unpkg.com/live2d-widget-model-shizuku@1.0.5/assets/shizuku.model.json 
		小可爱（女）：https://unpkg.com/live2d-widget-model-koharu@1.0.5/assets/koharu.model.json 
		小可爱（男）：https://unpkg.com/live2d-widget-model-haruto@1.0.5/assets/haruto.model.json
		初音：https://unpkg.com/live2d-widget-model-miku@1.0.5/assets/miku.model.json
*/

import headerTop from "@/pages/layout/headerTop.vue";
import bodyLeft from "@/pages/layout/bodyLeft.vue";
import bodyRight from "@/pages/layout/bodyRight.vue";
import backTop from "@/components/main/backTop.vue"
export default {
  name: "App",
  data() {
    return {};
  },

  created() {
    window.L2Dwidget.init({
      model: {
        jsonPath:
        //  "https://unpkg.com/live2d-widget-model-chitose@1.0.5/assets/chitose.model.json",
          // "https://unpkg.com/live2d-widget-model-shizuku@1.0.5/assets/shizuku.model.json",
         'https://unpkg.com/live2d-widget-model-haruto@1.0.5/assets/haruto.model.json',
          // "https://unpkg.com/live2d-widget-model-koharu/assets/koharu.model.json",
        // "https://unpkg.com/live2d-widget-model-ni-j/assets/ni-j.model.json",
        scale: 1,
      },
      display: {
        position: "right",
        width: 180,
        height: 300,
        hOffset: 70,
        vOffset: -20,
      },
      mobile: {
        show: true,
        scale: 0.5,
      },
      react: {
        opacityDefault: 0.7,
        opacityOnHover: 0.2,
      },
      dialog: {
        enable: true,
        script: {
          //每20s，显示一言（调用一言Api返回的句子）
          "every idle 20s": "$hitokoto$",
          //触摸到class='star'对象
          "hover .star": "星星在天上而你在我心里 (*/ω＼*)",
          //触摸到身体
          "tap body": "害羞⁄(⁄ ⁄•⁄ω⁄•⁄ ⁄)⁄",
          //触摸到头部
          "tap face": "~~",
        },
      },
    });
  },
  components: {
    headerTop,
    bodyLeft,
    bodyRight,
    backTop
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
      height: inherit;
  .body_box {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    padding: 32px 80px 0;
    margin-top: 64px;
    box-sizing: border-box;
    width: 100%;
    background: #666;
    height: auto;
    .box_middle {
      padding: 0 32px;
      max-width: 1440px;
      width: 100%;
      .language {
        width: 100%;
        height: 48px;
        background: #fff;
        border-radius: 5px;
        margin-bottom: 32px;
        display: flex;
        align-items: center;
        .lang {
          display: flex;
          align-items: center;
          .lang_txt {
            color: red;
            cursor: pointer;
          }
          li {
            margin-right: 10px;
          }
        }
        .pen {
          margin-left: 20px;
          height: 20px;
          margin-right: 10px;
        }
      }
    }
  }
}
</style>
