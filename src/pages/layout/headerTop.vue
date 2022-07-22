<template>
  <div class="header_box">
    <div class="header_left">左</div>
    <div class="header_middle">junjun</div>
    <div class="header_right">icon</div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  mounted() {
    
  },
  components: {},
  methods: {
   
  },
};
</script>
<style lang="scss">
.header_box{
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 65px;
    background: red;
    width: 100%;
    position: fixed;
    top: 0;
    z-index: 10;
}
</style>
