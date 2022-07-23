<template>
  <div class="detail_box">
    <detail />
 <buttom/>
  </div>
</template>

<script>
import buttom from "@/components/xxlbox/buttom.vue"
import detail from "@/components/detail/index.vue";
export default {
  components: {
    detail,
    buttom
  },
};
</script>

<style lang="scss" scoped>
.detail_box {
}
</style>