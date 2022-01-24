<template>
  <div id="app" class="body">
    <Header></Header>
    <router-view class="aaa"/>
    <Foot></Foot>
  </div>
</template>
<script>

  import Header from "./components/Header";
  import Foot from "./components/Foot";
  export default {
    components: {Foot, Header}
  }

</script>

<style lang="less">
  @import 'resources/font.css';
  .body{
    font-family: MSYH;
  }
  .aaa {
    background-color: #efefef;
    min-height: 100%;
  }
  #app {
    background-color: #efefef;
    height: 500vh;
    width: 100vw;
  }


</style>
