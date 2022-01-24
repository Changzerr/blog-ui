<template>
    <div class="announcement">
        <div class="title">
            网站公告
        </div>
        <div class="content">
            欢迎来到我的博客
        </div>
    </div>
</template>

<script>
    export default {
        name: "Announcement"
    }
</script>

<style scoped>
    .announcement{
        margin-top: 6%;
        margin-left: 2vw;
        width: 25vw;
        height: 65vh;
        background-color: #ffffff;
        border:#CCC solid 1px;
    }
    .title{
        font-weight: bold;
        font-size: 2vw;
        width: 100%;
        height: 24%;
        line-height: 18vh;/*让黄色div中的文字内容垂直居中*/
        text-align: center;/*让文字水平居中*/
        border-bottom: #888888 solid 1px ;
    }
    .content{
        font-weight: inherit;
        font-size: 3vh;
        width: 100%;
        height: 24%;
        line-height: 18vh;/*让黄色div中的文字内容垂直居中*/
        text-align: center;/*让文字水平居中*/
    }
    .announcement:hover {
        box-shadow: 0px 0px 5px #888888;/* 边框阴影 */
        -moz-box-shadow: 0px 0px 5px #888888; /* 老的 Firefox */  }
</style>
