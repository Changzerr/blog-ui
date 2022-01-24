<template>
    <div>
        <el-calendar class="calendar">
        </el-calendar>
    </div>
</template>

<script>
    export default {
        name: "Calendar",
    }
</script>

<style scoped>
    .calendar /deep/  .el-calendar-table .el-calendar-day{
        height: 6vh;
    }
    .calendar{
        margin-top: 2vw;
        margin-left: 2vw;
        width: 25vw;
    }

</style>
