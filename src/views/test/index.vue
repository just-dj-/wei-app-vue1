<template>
    <div class='testIndex'></div>
</template>

<script>
export default {
    name: 'testIndex',
    title: '测试首页',
    components: {},
    computed: {},
    props: {
        Data: {
            type: Object,
            twoWay: true,
            default: () => ({})
        }
    },
    data() {
        return {
            test: ''
        }
    },
    created() {
    },
    updated() {
    },
    mounted() {
    },
    methods: {},
    watch: {},
    destroyed() {
    }
}
</script>

<style scoped>

</style>