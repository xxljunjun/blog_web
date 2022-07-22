<template>
  <div class="box_left">
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
<style lang="scss">
.box_left {
  position: sticky;
  top: 0;
  z-index: 9;
}
</style>
