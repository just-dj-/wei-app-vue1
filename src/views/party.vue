<template>
    <div style="height: 100%">
        <div>
            <v-header></v-header>
        </div>
        <div style="display: inline-flex; width: 100%; height: 100%;">
            <v-leftMenu></v-leftMenu>
            <v-main></v-main>
        </div>
    </div>
</template>

<script>
    import header from '@/views/header.vue';
    import leftMenu from '@/views/leftMenu.vue';
    import main from '@/views/main.vue';
    export default {
        name: "",
        data() {
          return {

          }
        },

        components: {
            'v-header': header,
            'v-leftMenu': leftMenu,
            'v-main': main,
        }
    }
</script>

<style>

</style>