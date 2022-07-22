<template>
   <xxlbox title="近期文章" imgsrc="record">
    <div class="home">
      <div v-for="item in tableList" :key="item.id" class="txt_box">
        <h3 class="titile">数据结构之栈 Stack 和队列 Queue</h3>
        <p class="txt_content">
           <img src="@/assets/icons/file.png" class="icon"/>
           <span>2020-04-23</span>
           <img src="@/assets/icons/file.png" class="icon"/>
           <span>2020-05-28</span>
           <img src="@/assets/icons/file.png" class="icon"/>
           <span>数据结构与算法</span>
        </p>
        <p class="txt"> 栈（Stack）和队列（Queue），了解栈和队列的基础知识.</p>
      </div>
      <div class="more">更多文章</div>
    </div>
  </xxlbox>
</template>
<script>
import xxlbox from "@/components/xxlbox/xxlbox.vue";
export default {
  data(){
    return {
      tableList:[
        {id:1},
          {id:2},
            {id:3},
              {id:4}
      ]
    }
  },
   components: {
    xxlbox,
  },
};
</script>
<style lang="scss" scoped>
.home{
  .txt_box{
    height: 180px;
    background: #fff;
    padding: 32px;
    box-sizing: border-box;
    .titile{
      color: red;
      font-size: 24px;
      margin-bottom: 20px;
    }
    .txt_content{
      display: flex;
      align-items: center;
      margin-bottom: 20px;
      .icon{
        height: 20px;
        margin-right: 5px;
      }
      span{
        margin-right: 20px;
      }
    }
    .txt{

    }
  }
  .more{
    height: 52px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: red;
    font-size: 20px;
    border-top: 2px solid red;
    &:hover{
      color: #fff;
      background: red;
      cursor: pointer;
    }
  }
}
</style>
