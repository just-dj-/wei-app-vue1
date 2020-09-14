<template>
    <div style="width: 100%; height: 500px;">
        <div style="height: 300px; padding: 5px" v-for="(user,i) in userList" :key="i"  :class="i === 0||i===1 ? 'style1' : 'style2'">
            <div style="border: 2px solid #d3d3d34d;" >
                <div style="height: 15%; text-align: left; line-height: 50px; margin-left: 15px">
                    {{user.title}}
                </div>
                <div style="height: 70%; text-align: center">
                    <div style="display:inline-block; vertical-align: middle; padding: 8px">
                        <!--<img src="../assets/images/head.png" style="height: 60px">-->
                        <img :src="require('../assets/images/' + user.icon)" height="60px">
                    </div>
                    <div style="display:inline-block; vertical-align: middle; line-height: 190px">
                        {{user.num}} {{user.unit}}
                    </div>
                </div>
                <div style="height: 10%; background-color: #d3d3d34d">
                    本月新增：{{user.increment}} {{user.unit}}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import axios from 'axios'
    export default {
        name: "",
        components: {
        },
        data() {
            return {
                userList: null
            }
        },
        // 初始化记载
        created() {
            let vue = this;
            vue.getUserList();
        },
        // DOM加载完毕执行操作
        mounted() {

        },
        // 事件处理
        methods: {
            getUserList() {
                axios.get('/data/cardList.json').then(response => {
                    console.log(response.data);
                    let vue = this;
                    vue.userList = response.data;
                });
            }
        },
        // 离开路由的操作
        destroyed() {

        }
    }
</script>

<style scoped>
    .style1 {
        float: left;
        width: 45.5%;
        margin-left: 10px;
        /*color: #42b983;*/
    }
    .style2 {
        float: left;
        margin-left: 10px;
        width: 22%;
        /*color: rebeccapurple;*/
    }

</style>