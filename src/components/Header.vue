<template>
    <div class="head">
        <div class="title">
            BLOG
        </div>
        <el-menu
                :default-active="activeIndex2"
                class="el-menu-demo"
                mode="horizontal"
                @select="handleSelect"

                background-color="#1b1c1d"
                text-color="#fff"
                active-text-color="#ffd04b"
                id="header">

            <el-menu-item index="1">
                <router-link to="/">Home</router-link>
            </el-menu-item>
            <el-submenu index="2">
                <template slot="title">
                    分类
                </template>
                <el-menu-item index="2-1">
                    <router-link to="/about">About</router-link>
                </el-menu-item>
                <el-menu-item index="2-2">选项2</el-menu-item>
                <el-menu-item index="2-3">选项3</el-menu-item>
            </el-submenu>
            <el-menu-item index="3">
                <router-link to="/about">归档</router-link>
            </el-menu-item>
            <el-menu-item index="4">友人帐</el-menu-item>
            <el-menu-item index="5">关于我</el-menu-item>
        </el-menu>
    </div>

</template>

<script>


    export default {
        name: "Header",
        data() {
            return {
                activeIndex: "1",
                activeIndex2: "1",
            };
        },
        methods: {
            handleSelect(key, keyPath) {
                console.log(key, keyPath);
            },
            btn_pos:function(){
                //滚动条的高度
                // let pathName =  this.$route.path;
                // console.log(pathName);
                // if(pathName==="/"){
                //     var scrollTop = document.body.scrollTop || document.documentElement.scrollTop;
                //     var clientHeight=document.documentElement.clientHeight;
                //     //滚动条的高度>可视区的高度
                //     if(scrollTop>clientHeight){
                //         header.style.backgroundColor="#1b1c1d"
                //     }else{
                //         header.style.backgroundColor="transparent"
                //     }
                // }else{
                //     header.style.backgroundColor="#1b1c1d"
                // }

            }
        },
        mounted(){

            window.addEventListener('scroll',this.btn_pos);
        },
        destroyed () {
            //离开这个界面之后，删除，不然会有问题
            window.removeEventListener('scroll', this.btn_pos)
        }
    };

</script>

<style scoped>

    .title{
        color: white;
        font-size: 2.5vw;
        line-height: 11vh;/*让黄色div中的文字内容垂直居中*/
        text-align: center;/*让文字水平居中*/
        float: left;
        width: 15vw;
        height: 100%;
    }
    .head{
        position: fixed;
        left: 0;
        top: 0;
        width: 100%;
        height: 11vh;
        z-index: 100;
        background-color: #1b1c1d;
        z-index: 100;
    }
    .el-menu-demo{
        float: left;
        width: 60vw;
        height: 11vh;
        z-index: 100;
    }
    /*}*/
    /* 点击出来的下划线进行隐藏 */
    .el-menu-item.is-active {
        border-bottom: none!important;
        color: rgba(0,0,0,0);

    }
    /* 整体的下划线进行隐藏 */
    .el-menu.el-menu--horizontal{
        border-bottom: none;
    }
    /* 导航栏的间距等样式 */
    .el-menu-item {
        padding: 0 40px;
        font-size: 16px;

    }

</style>


