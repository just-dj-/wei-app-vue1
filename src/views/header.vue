<template>
    <div style="height: 100%; width:100%; color: white; background-color: red;">
        <div style="margin-left: 20px; float: left;  width: 240px; line-height: 60px">
                <span>
                    <i class="el-icon-edit"></i>
                </span>
            <span>
                微信版党建测试企业
            </span>
        </div>
        <!--<div class="line" style="border-color: red; border-width: 12px"></div>-->
        <div style="margin-left: 240px">
            <el-menu
                    :default-active="activeIndex2"
                    class="el-menu-demo"
                    mode="horizontal"
                    @select="handleSelect"
                    background-color="red"
                    text-color="#fff"
                    active-text-color="#ffd04b">
                <el-menu-item index="1">系统管理</el-menu-item>
                <el-menu-item index="2">
                    <a href="https://www.ele.me" target="_blank">默认分类</a>
                </el-menu-item>

                <div style="float: right; margin-top: 17px; margin-right: 5px">
                    <button style="color: white; background-color: burlywood">
                        退出
                    </button>
                </div>
            </el-menu>
        </div>
    </div>
</template>

<script>
    export default {
        name: ""
    }
</script>

<style scoped>

</style>