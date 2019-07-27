<template>
    <div class="sub-kind-main">
        <div class="header-bar">
            <button @click="$router.go(-1)">&lt;{{$route.params.subKindId}}</button>
        </div>
        <h2>THIS IS  subkind</h2>
        <router-link class="img-block" tag="div" :to="{name:'goodsDetail',params:{subKindId:$route.params.subKindId,id:1}}">图1</router-link>
        <router-link class="img-block" tag="div" :to="{name:'goodsDetail',params:{subKindId:$route.params.subKindId,id:2}}">图2</router-link>

    </div>
</template>
<script>
import axios from 'axios'
export default {
    created(){
        axios.get('/data.json')
            .then(res=>{
                console.log(res);
            })
    }
}
</script>
<style lang="scss" scoped>
    .header-bar{
        position: fixed;
        left: 0;
        top: 0;
        width: 100%;
        height: 44px;
        background: #f5f5f5;
        z-index: 999;
    }
    .img-block{
        float: left;
        width: 140px;
        height: 140px;
        margin:20px;
        border: 1px solid rebeccapurple;
    }
</style>

