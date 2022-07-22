<template>
  <xxlbox title="菜单" imgsrc="menu">
    <ul class="tab">
      <li v-for="item in tabBarList" :key="item.id">
        <router-link tag="div" :to="item.path" class="tab_box">
         <div>
           <img src="@/assets/icons/home.png" alt="" class="icon" />
          
            {{ item.tabName }}
         </div>
          
        <div class="red_box"></div>
        </router-link>
      </li>
    </ul>
  </xxlbox>
</template>
<script>
import xxlbox from "@/components/xxlbox/xxlbox.vue";
export default {
  data() {
    return {
      tabBarList: [
        { id: 1, tabName: "首页", path: "/",isChoose:true},
      ],
    };
  },
  mounted() {},
  components: {
    xxlbox,
  },
  methods: {},
};
</script>
<style lang="scss" scoped>
.tab {
  li {
    height: 50px;
    padding: 0 20px;
    cursor: pointer;
    &:hover {
      background: #eee;
    }
    .tab_box {
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 50px;
      .icon {
        height: 20px;
        margin-right: 5px;
      }
    }
    .red_box {
      height: 15px;
      width: 15px;
      border: 2px solid #fff;
      border-radius: 4px;
      background: red;
    }
  }
}
</style>
