<template>
  <div class="homeIndex">
    <xxlbox title="礼仪" imgsrc="heart">
      <div class="word_box">
        <p class="word">
          <typingEffect />
        </p>
        <div class="myName">--junjunL--</div>
      </div>
    </xxlbox>
    <xxlbox title="近期文章" imgsrc="record">
      <div class="home">
        <div
          v-for="item in tableList"
          :key="item.id"
          class="txt_box"
          @click="goToDetail"
        >
          <h3 class="titile">数据结构之栈 Stack 和队列 Queue</h3>
          <p class="txt_content">
            <img src="@/assets/icons/time_2.png" class="icon" />
            <span>2020-04-23</span>
            <img src="@/assets/icons/time_3.png" class="icon" />
            <span>2020-05-28</span>
            <img src="@/assets/icons/file.png" class="icon" />
            <span class="mylabel">数据结构与算法</span>
          </p>
          <p class="txt">栈（Stack）和队列（Queue），了解栈和队列的基础知识.</p>
        </div>
        <div class="more">更多文章</div>
      </div>
    </xxlbox>
    <mybuttom />
  </div>
</template>
<script>
import mybuttom from "@/components/xxlbox/mybuttom.vue";
import xxlbox from "@/components/xxlbox/xxlbox.vue";
import typingEffect from "@/components/main/typingEffect.vue";
export default {
  data() {
    return {
      tableList: [
        { id: 1 },
        { id: 2 },
        { id: 3 },
        { id: 4 },
        { id: 5 },
        { id: 6 },
        { id: 7 },
        { id: 8 },
        { id: 9 },
      ],
    };
  },
  components: {
    xxlbox,
    typingEffect,
    mybuttom,
  },
  methods: {
    goToDetail() {
      this.$router.push("/detail");
    },
  },
};
</script>
<style lang="scss" scoped>
@media screen and (max-width: 800px) {
  .home {
    .txt_box {
     min-height: 60px !important  ;
      .titile {
        
      }
      .txt_content {
       
        .icon {
         height: 10px !important;
      margin-right: 4px !important;
        }
        span {
          
        }
        .mylabel {
          
        }
      }
      .txt {
      }
    }
    .more {
      min-height: 20px;
    }
  }
}
.homeIndex {
  .word_box {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding-bottom: 40px;
    margin: 20px 0 0;
    height: 150px;
    .word {
      position: relative;
      width: 100%;
      text-align: center;
      font-size: 20px;
      &::before {
        content: "『";
        position: absolute;
        left: 20px;
        top: -20px;
      }
      &::after {
        content: "』";
        position: absolute;
        right: 20px;
        bottom: -20px;
      }
    }
    .myName {
      margin-top: 50px;
    }
  }
}
.home {
  .txt_box {
    min-height: 180px;
    background: #fff;
    padding: 32px;
    box-sizing: border-box;
    border-bottom: 1px solid #ccc;
    &:hover {
      background: #eee;
      cursor: pointer;
    }
    .titile {
      color: red;
      font-size: 24px;
      margin-bottom: 20px;
      &:hover {
        text-decoration: underline;
      }
    }
    .txt_content {
      display: flex;
      align-items: center;
      margin-bottom: 20px;
      .icon {
        height: 20px;
        margin-right: 5px;
      }
      span {
        margin-right: 20px;
      }
      .mylabel {
        color: #09f;
        font-weight: 600;
        &:hover {
          text-decoration: underline;
        }
      }
    }
    .txt {
    }
  }
  .more {
    height: 52px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: red;
    font-size: 20px;
    border-top: 2px solid red;
    &:hover {
      color: #fff;
      background: red;
      cursor: pointer;
    }
  }
}
</style>
