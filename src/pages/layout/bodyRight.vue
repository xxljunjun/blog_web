<template>
  <div class="bodyRight">
    <sort/>
  </div>
</template>
<script>
import sort from "@/components/xxlbox/sort.vue";
export default {
  data() {
    return {};
  },
  mounted() {},
  components: {
   sort
  },
  methods: {},
};
</script>
<style lang="scss" scoped>
.bodyRight {
  padding-bottom:32px ;
  position: sticky;
  top: 0;
  z-index: 9;
}
</style>
