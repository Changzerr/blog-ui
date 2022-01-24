<template>
    <div class="pagination">
        <el-pagination class="page"
                background
                layout="prev, pager, next"
                :total="11">
        </el-pagination>
    </div>
</template>

<script>
    export default {
        name: "Pagination",
        methods: {
            handleSizeChange(val) {
                console.log(`每页 ${val} 条`);
            },
            handleCurrentChange(val) {
                console.log(`当前页: ${val}`);
            }
        },
        data() {
            return {
                currentPage4: 4
            };
        }
    }
</script>

<style scoped>
    .pagination{
        text-align: center;
        width: 100%;
        height: 20%;
        margin-top: 6vh;
    }
</style>
