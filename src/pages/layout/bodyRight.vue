<template>
  <div class="box_left">
    <mine />
    <mine />
  </div>
</template>
<script>
import mine from "@/components/mine.vue";
export default {
  data() {
    return {};
  },
  mounted() {},
  components: {
    mine,
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
