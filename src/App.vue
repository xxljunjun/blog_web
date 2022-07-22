<template>
  <div class="app_box">
    <headerTop />
    <div class="body_box">
     <!-- <div class="box"> -->
         <bodyLeft />
      <!-- </div> -->
     
      <div class="box_middle">
        <div class="language"></div>
        <router-view></router-view>
      </div>
      <!-- <div class="box"> -->
         <bodyRight />
      <!-- </div> -->
     
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
  background: #eee;
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
        background: red;
        border-radius: 5px;
        margin-bottom: 32px;
      }
    }
  }
}
</style>
