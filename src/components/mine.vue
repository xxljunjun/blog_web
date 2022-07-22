<template>
  <div class="mine">
    <img src="@/assets/logo.png" alt="" class="avatar">
    <div class="line"></div>
    <ul class="maessage">
      <li class="myName">junjun</li>
      <li class="txt">问题, 方法, 程序, 标准, 解决</li>
      <li class="numbers">
        <span>15</span>
        <span>|</span>
        <span>18</span>
        <span>|</span>
        <span>24</span>
      </li>
      <li class="connect">
        <span>1</span>
        <span>1</span>
        <span>1</span>
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
  components: {
    
  },
  methods: {},
};
</script>
<style lang="scss">
.mine {
 height: 450px;
 width: 260px;
 background: #fff;
 border-radius: 5px;
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: flex-start;
  margin-bottom: 32px;
 .avatar{
  height: 228px;
  width: 228px;
 }
 .line{
  height: 0;
  width: 100%;
  border-bottom:#000000 3px dashed;/*#000000表示白色，边框宽度为一个像素，边框线型为虚线*/
  
 }
 .maessage{
  display: flex;
  flex-direction: column;
  align-items: center;
  li{
    margin: 15px 0;
  }
  .myName{

  }
  .txt{

  }
  .numbers{

  }
  .connect{

  }
 }
}
</style>
