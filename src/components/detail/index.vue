<template>
  <pageBox title="页面内容" imgsrc="record">
    <div class="detail">
      <div class="title">算法之基础</div>
      <p class="txt_content">
        <img src="@/assets/icons/time_2.png" class="icon" />
        <span>2020-04-23</span>
        <img src="@/assets/icons/time_3.png" class="icon" />
        <span>2020-05-28</span>
        <img src="@/assets/icons/file.png" class="icon" />
        <span class="mylabel">数据结构与算法</span>
        <img src="@/assets/icons/fire.png" class="icon" />
        <span>999</span>
      </p>
      <div class="outline">
        算法基础，了解算法的基础知识，算法的种类，知道什么是好算法。
      </div>
      <div class="content">
        <div :id="`content_${item.id}`" v-for="item in textArr" :key="item.id">
          <div class="headline">算法特性</div>
          <div class="txt">
            栈Stack是一种线性结构，是线性表的一种具体形式。栈这种后进先出（Last
            In First
            Out，LIFO）的应用非常广泛，例如网页的前进后退功能，编辑器的后一步前一步功能，方法调用时的函数栈等等。
          </div>
        </div>
      </div>
      <div class="refer">
        <div class="txt">本文参考：</div>
        <div class="text_box">
          <div class="referText">【C语言描述】《数据结构和算法》（小甲鱼）</div>
        </div>
      </div>
    </div>
    <ending/>
    <buttom/>
  </pageBox>
</template>

<script>
import pageBox from "@/components/main/pageBox.vue";
import ending from "@/components/main/ending.vue";

export default {
  data() {
    return {
      textArr: [{ id: 1 }],
    };
  },
  components: {
    pageBox,
    ending,
    
  },
};
</script>

<style lang="scss" scoped>
.detail {
  padding: 0 32px;
  .title {
    font-size: 40px;
    // font-weight: 600;
    text-align: center;
    padding-bottom: 20px;
    border-bottom: 3px solid #eee;
    margin-top: 40px;
  }
  .txt_content {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 20px 0 0;
    .icon {
      height: 20px;
      margin-right: 8px;
    }
    span {
      margin-right: 25px;
    }
    .mylabel {
      color: red;
      &:hover {
        text-decoration: underline;
      }
    }
  }
  .outline {
    margin: 50px 0;
  }
  .content {
    padding-bottom: 50px;
    #content_1 {
      .headline {
        font-weight: 600;
        font-size: 32px;
        padding-bottom: 20px;
        border-bottom: 3px solid #eee;
        margin-bottom: 20px;
      }
    }
  }
  .refer {
    display: flex;
    padding-bottom: 50px;
    .text_box {
      .referText {
        color: #09f;
        cursor: pointer;
      }
    }
    .txt {
            font-size: 16px;
    word-wrap: break-word;
    }
  }
}
</style>