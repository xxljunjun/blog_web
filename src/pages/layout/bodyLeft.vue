<template>
  <div class="bodyLeft">
    <mine />
    <navigation/>
  </div>
</template>
<script>
import mine from "@/components/mine.vue";
import navigation from "@/components/xxlbox/navigation.vue";
export default {
  data() {
    return {};
  },
  mounted() {},
  components: {
    mine,
    navigation
  },
  methods: {},
};
</script>
<style lang="scss" scoped>
.bodyLeft {
  width: 260px;
  padding-bottom:32px ;
  position: sticky;
  top: 0;
  z-index: 9;
}
</style>
