<template>
    <div class="overview">
        <h2 style="text-align: center;">ArrayList的扩容机制</h2>
        <div class="msg">
            <span style="margin-right: 2vw;color: #00a7e0"><i class="iconfont icon-rili"></i> 2022-01-24</span>
            <span style="margin-right: 1vw;color: #ff3f1f"><i class="iconfont icon-browse"></i> 270</span>
            <span style="color: #ff3f1f"><i class="iconfont icon-dianzan"></i> 17</span>
        </div>
        <p>ArrayList：作为 List 接口的主要实现类；线程不安全，效率高；底层使用Object[] elementData 存储，本文以ArrayList()为例，来介绍ArrayList的扩容机制。</p>

        <div class="img">
            <img src="../resources/2.jpg">
        </div>
        <div class="buttonBox">
            <el-button type="primary" round class="button">阅读全文</el-button>
            <div class="tag">
                <Tags></Tags>
                <Tags></Tags>
            </div>
        </div>

    </div>
</template>

<script>
    import Tags from "./Tags";
    export default {
        name: "Overview",
        components: {
            Tags
        },
    }
</script>

<style scoped>
    .msg{
        text-align: right;
        margin-right: 5%;
    }
    .buttonBox{
        text-align: center;
        margin-top: 1%;
        margin-bottom: 6%;
    }
    img{
        width: 90%;
        margin: 0 auto;
    }
    .img{
        text-align: center;
        width: 60vw;
    }
    p{
        margin-left: 5%;
        width: 90%;
    }
    .overview{
        margin-top: 3%;
        width: 60vw;
        background-color: #fffdfe;
        /*float: right;*/
        border:#CCC solid 1px
    }
    .tag{
        margin-left: 2%;
        margin-top: 1%;
        margin-bottom: 1%;
        border-top: 1px solid #CCC;
    }
    .overview:hover {
        box-shadow: 0px 0px 5px #888888;/* 边框阴影 */
        -moz-box-shadow: 0px 0px 5px #888888; /* 老的 Firefox */  }

    @font-face {
        font-family: "iconfont"; /* Project id 2972274 */
        src: url('//at.alicdn.com/t/font_2972274_lapr9chp3y.woff2?t=1643031378300') format('woff2'),
        url('//at.alicdn.com/t/font_2972274_lapr9chp3y.woff?t=1643031378300') format('woff'),
        url('//at.alicdn.com/t/font_2972274_lapr9chp3y.ttf?t=1643031378300') format('truetype');
    }

    .iconfont {
        font-family: "iconfont" !important;
        font-size: 16px;
        font-style: normal;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }

    .icon-browse:before {
        content: "\e6e0";
    }

    .icon-rili:before {
        content: "\e8cf";
    }

    .icon-dianzan:before {
        content: "\ec7f";
    }

    .icon-github-fill:before {
        content: "\e885";
    }

</style>
