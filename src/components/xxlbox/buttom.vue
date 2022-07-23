<template>
    <xxlbox :hasTop="false">
        <div class="buttom">
            <p>© 2022 - 2022 junjunL</p>
             <p>由vue强力驱动</p>
        </div>
    </xxlbox>
</template>

<script>
import xxlbox from "@/components/xxlbox/xxlbox.vue";
    export default {
        components: {
    xxlbox,
  },
    }
</script>

<style lang="scss" scoped>
.buttom{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 20px;
    p{
        margin-bottom: 10px;
    }
}
</style>