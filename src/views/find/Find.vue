<template>
    <div class="find-main">
        <div class="header-bar">
            <router-link to="/find/article">精选文章</router-link>
            <router-link to="/find/goods">好物推荐</router-link>
        </div>
        
        <hr>
        <router-view></router-view>
    </div>
</template>
<script>

export default {
    name: 'Find',
    components:{
    }


}
</script>
<style scoped lang="scss">
    .header-bar{
        position: fixed;
        left: 0;
        top: 0;
        z-index: 999;
        background-color: green;
        text-align: center;
        a{
            display: inline-block;
        }
    }
</style>

