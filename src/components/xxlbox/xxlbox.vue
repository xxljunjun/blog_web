<template>
  <div class="box">
    <div class="top_box" :style="`width:${width}`" v-if='hasTop'>
      <div class="left_box">
        <img :src="require('@/assets/icons/'+imgsrc+'.png')" alt="xxljunjun" class="menu" />
        {{ title }}
      </div>
      <div class="right_box" @click="changStatus">
        <img
          src="@/assets/icons/reduce.png"
          alt="xxljunjun"
          title="收起"
          class="reduce"
          v-if="status"
        />
        <img
          src="@/assets/icons/add.png"
          alt="xxljunjun"
          title="展开"
          class="add"
          v-else
        />
      </div>
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
  props: {
    title: {
      type: String,
      default: "",
    },
    imgsrc: {
      type: String,
      default: "menu",
    },
    width:{
      type:String,
      default:"100%"
    },
     hasTop:{
      type:Boolean,
      default:true
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
<style lang="scss" scoped>
.box {
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
      .menu {
        height: 16px;
        position: relative;
        top: 3px;
      }
    }
    .right_box {
      .reduce {
        height: 16px;
        cursor: pointer;
      }
      .add {
        height: 16px;
        cursor: pointer;
      }
    }
  }
  .content {
   
  }
}
</style>
