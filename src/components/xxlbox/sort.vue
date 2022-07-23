<template>
  <xxlbox title="分类" imgsrc="file" width="260px">
    <div class="sort_box">
     <div v-for="item in txtList" :key="item.id" class="item">{{item.txt}}</div>
    </div>
  </xxlbox>
</template>
<script>
import xxlbox from "@/components/xxlbox/xxlbox.vue";
export default {
  data() {
    return {
      txtList: [
        { id: 1, txt: "Blog"},
        { id: 1, txt: "Hexo"},
        { id: 1, txt: "网络"},
        { id: 1, txt: "Note"},
        { id: 1, txt: "SQL"},
        { id: 1, txt: "Markdown"},
        { id: 1, txt: "数据结构与算法"},
        { id: 1, txt: "Plugin"},
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
.sort_box{
  display: flex;
  flex-wrap: wrap;
  padding: 10px;
  // box-sizing: border-box;
  .item{
    padding-right: 10px;
    margin-bottom: 15px;
  }
}
</style>
