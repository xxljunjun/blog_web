<template>
  <div class="box_left">
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
<style lang="scss">
.box_left {
  padding-bottom:32px ;
  position: sticky;
  top: 0;
  z-index: 9;
}
</style>
