<template>
  <xxlbox title="菜单" imgsrc="menu" width="260px">
    <ul class="tab">
      <li
        v-for="item in tabBarList"
        :key="item.id"
        :class="{ bgm: item.isChoose }"
      >
        <router-link tag="div" :to="item.path" class="tab_box">
          <div>
            <img :src="item.isChoose?item.activityImgUrl:item.imgUrl" alt="" class="icon" />

            {{ item.tabName }}
          </div>

          <div class="red_box" v-if="item.isChoose"></div>
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
        {
          id: 1,
          tabName: "首页",
          path: "/",
          isChoose: false,
          imgUrl: require("@/assets/icons/home.png"),
          activityImgUrl: require("@/assets/icons/home_w.png"),
        },
        // {
        //   id: 2,
        //   tabName: "关于",
        //   path: "/about",
        //   isChoose: false,
        //   imgUrl: require("@/assets/icons/about.png"),
        //   activityImgUrl: require("@/assets/icons/about_w.png"),
        // },
      ],
    };
  },
  watch: {
    "$route.path": {
      handler(newVal) {
        this.tabBarList.forEach((val) => {
          if (val.path == newVal) {
            val.isChoose = true;
          } else {
            val.isChoose = false;
          }
        });
      },
      immediate: true,
    },
  },
  mounted() {
    
  },
  components: {
    xxlbox,
  },
  methods: {},
};
</script>
<style lang="scss" scoped>
.tab {
  .bgm {
    background: #333 !important;
    color: #fff;
  }
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
