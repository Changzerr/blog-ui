<template>
  <div class="home">
    <img src="../resources/1.png" width=100%>
    <div class="main">
      <div class="widget">
        <Announcement></Announcement>

        <Calendar></Calendar>
      </div>
      <div class="mainBlog">
        <Overview></Overview>
        <Overview></Overview>
        <Overview></Overview>
        <Overview></Overview>
        <Overview></Overview>
        <div class="pagination">
          <Pagination></Pagination>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Calendar from "../components/Calendar";
import Announcement from "../components/Announcement";
import Overview from "../components/Overview";
import Pagination from "../components/Pagination";
import Foot from "../components/Foot";

export default {
  name: "Home",
  components: {
    Foot,
    Overview,
    Announcement,
    Calendar,
    HelloWorld,
    Pagination,

  },
};
</script>
<style>
  .widget {
    width: 30vw;
    /*float: left;*/

  }
  .home{
    margin-top: 10vh;
    /*flex-direction: column;*/
  }
  .main{
    display: flex;

  }
  .mainBlog{
    margin-right: 8vw;
    margin-top: 0;
    margin-bottom: 3%;
    width: 60vw;

    /*height: 70vh;*/
    /*float: right;*/
  }


</style>
