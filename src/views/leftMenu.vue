<template>
    <div style="width: 250px; background-color: #e9e5e5; height: 100%;">
        <div style="height: 40px">
            <el-input
                    placeholder="导航菜单"
                    prefix-icon="el-icon-search"
                    v-model="input21"
                    style=" height: 80%; width: 80%; line-height: 30px">
            </el-input>
        </div>
        <div style="height: 50px; text-align: left; line-height: 50px;
            background-color: #f3dcc4; color: red">
            <span style="margin-left: 40px; margin-top: 20px">
                <i class="el-icon-edit"></i>
            </span>
            <span>
                概览
            </span>
        </div>
        <div>
            <el-row class="tac">
                <el-col class="tac">
                    <el-menu
                            default-active="2"
                            class="el-menu-vertical-demo"
                            @open="handleOpen"
                            @close="handleClose"
                            background-color="#e9e5e5"
                            active-text-color="#ffd04b">
                        <el-submenu index="1">
                            <template slot="title" >
                                <i class="el-icon-location"></i>
                                <span>党员党组织</span>
                            </template>
                            <el-menu-item index="1-1">党组织管理</el-menu-item>
                            <el-menu-item index="1-2">党员信息</el-menu-item>
                        </el-submenu>
                    </el-menu>
                </el-col>
            </el-row>
        </div>
    </div>
</template>

<script>
    export default {
        name: "",
        methods: {
            handleOpen(key, keyPath) {
                console.log(key, keyPath)
            },
            handleClose(key, keyPath) {
                console.log(key, keyPath)
            }
        }
    }
</script>

<style scoped>
    /deep/ .el-input__inner {
        height: 30px;
        margin-top: 5px;
    }
</style>