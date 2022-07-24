<template>
  <xxlbox title="分类" imgsrc="file">
    <div class="sort_box">
     <div v-for="item in txtList" :key="item.id" class="item" :class="`activity_${item.myCn}`">{{item.txt}}</div>
    </div>
  </xxlbox>
</template>
<script>
import xxlbox from "@/components/xxlbox/xxlbox.vue";
export default {
  data() {
    return {
      txtList: [
        { id: 1, txt: "Blog",myCn:1},
        { id: 2, txt: "Hexo",myCn:3},
        { id: 3, txt: "网络",myCn:2},
        { id: 4, txt: "Note",myCn:2},
        { id: 5, txt: "SQL",myCn:1},
        { id: 6, txt: "Markdown",myCn:3},
        { id: 7, txt: "数据结构与算法",myCn:1},
        { id: 8, txt: "Plugin",myCn:2},
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
.activity_1{
  font-size: 14px;
  color: #666;
}
.activity_2{
  font-size: 16px;
  color: #d1d1d1;
}
.activity_3{
  font-size: 18px;
  color: #000;
}
.sort_box{
  display: flex;
  flex-wrap: wrap;
  padding: 10px;
  // box-sizing: border-box;
  .item{
    padding-right: 10px;
    margin-bottom: 15px;
    cursor: pointer;
    &:hover{
      text-decoration: underline;
    }
  }
}
</style>
