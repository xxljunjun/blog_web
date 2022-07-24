<template>
  <xxlbox :hasTop="false">
    <div class="mybuttom">
      <p>© 2022 - 2022 junjunL</p>
      <p>由vue强力驱动</p>
    </div>
  </xxlbox>
</template>

<script>
import xxlbox from "@/components/xxlbox/xxlbox.vue";
export default {
    name:"mybuttom",
  components: {
    xxlbox,
  },
};
</script>

<style lang="scss" scoped>

.mybuttom {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 20px;
  p {
    margin-bottom: 10px;
  }
}
</style>