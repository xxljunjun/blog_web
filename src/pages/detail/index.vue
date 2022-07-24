<template>
  <div class="detail_box">
    <detail />
 <mybuttom/>
  </div>
</template>

<script>
import mybuttom from "@/components/xxlbox/mybuttom.vue"
import detail from "@/components/detail/index.vue";
export default {
  components: {
    detail,
    mybuttom
  },
};
</script>

<style lang="scss" scoped>
.detail_box {
}
</style>