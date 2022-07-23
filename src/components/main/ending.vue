<template>
    <div class="ending">
        <p class="endingtxt">以上文章已结束<i class="el-icon-video-play"></i>感谢你的阅读</p>
        <p class="moretxt">请多多留言，您的建议将大大提高我的创作质量</p>
    </div>
</template>

<script>
    export default {
        data(){
            return{

            }
        },

    }
</script>

<style lang="scss" scoped>
.ending{
    border-top: 3px solid #eee;
    width: 100%;
    padding: 0 32px;
    box-sizing: border-box;
    p{
        text-align: center;
    }
    .endingtxt{
        font-size: 26px;
        color: #ccc;
        margin: 20px 0;
    }
    .moretxt{
        padding-bottom: 20px;
    }
}
</style>