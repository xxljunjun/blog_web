<template>
  <div class="box">
    <div class="top_box">
      <div class="left_box">{{title}}</div>
      <div class="right_box" @click="changStatus">+</div>
    </div>
    <div class="content" v-if="status">
      <slot></slot>
    </div>
  </div>
</template>
<script>
export default {
  name: "box",
  data() {
    return {
      status: true,
    };
  },
  props:{
    title:{
      type:String,
      default:''
    }
  },
  mounted() {},
  components: {},
  methods: {
    changStatus() {
      this.status = !this.status;
    },
  },
};
</script>
<style lang="scss">

.box {
  width: 260px;
  background: #fff;
  border-radius: 5px;
  margin-bottom: 32px;
  .top_box {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 38px;
  }
  .content{
    
  }
}
</style>
