<template>
    <div class="kind-main">
        <div class="header-bar">

        </div>
        <div class="kind-block-list">

         <kind-block  :active.sync="showKinds" :id="index" :kind="kind" v-for="(kind,index) in kinds" :key ="kind.ename"></kind-block>
        </div>
        <!-- <router-view></router-view> -->
    </div>
</template>
<script>
import KindBlock from './components/KindBlock.vue'
export default {
    name: 'Kind',
    components:{
        KindBlock
    },
    data(){
        return {
            kinds:[
                {
                    cname: '创意',
                    ename: 'changyi',
                    img: require('@/assets/imgs/kind/goods1.png'),
                    subKinds:[
                        {
                            cname:'全部',
                            id: Math.random()
                        },
                        {
                            cname:'睡衣',
                            id: Math.random()
                        },
                        {
                            cname:'浴袍',
                            id: Math.random()
                        },
                        {
                            cname:'其他',
                            id: Math.random()
                        },
                    ]
                },
                {
                    cname: '家居',
                    ename: 'jiaju',
                    img: require('@/assets/imgs/kind/goods2.png'),
                    subKinds:[
                        {
                            cname:'全部',
                            id: Math.random()
                        },
                        {
                            cname:'睡衣',
                            id: Math.random()
                        },
                        {
                            cname:'浴袍',
                            id: Math.random()
                        },
                        {
                            cname:'其他',
                            id: Math.random()
                        },
                    ]
                },
                {
                    cname: '服饰',
                    ename: 'fushi',
                    img: require('@/assets/imgs/kind/goods3.png'),
                    subKinds:[
                        {
                            cname:'全部',
                            id: Math.random()
                        },
                        {
                            cname:'睡衣',
                            id: Math.random()
                        },
                        {
                            cname:'浴袍',
                            id: Math.random()
                        },
                        {
                            cname:'其他',
                            id: Math.random()
                        },
                    ]
                },
                {
                    cname: '香氛',
                    ename: 'xiangfen',
                    img: require('@/assets/imgs/kind/goods4.png')
                },
                {
                    cname: '配饰',
                    ename: 'peishi',
                    img: require('@/assets/imgs/kind/goods5.png')
                },
                {
                    cname: '创意',
                    ename: 'changyi2',
                    img: require('@/assets/imgs/kind/goods1.png')
                },
                {
                    cname: '家居',
                    ename: 'jiaju2',
                    img: require('@/assets/imgs/kind/goods2.png')
                },

            ],
            showKinds:-1,
        }
    }


}
</script>
<style scoped lang="scss">
    .header-bar{
        position: fixed;
        left: 0;
        top: 0;
        width: 100%;
        height: 44px;
        background-color: aquamarine;
        z-index: 999;
    }
    .kind-block-list{
        width: 100%;
        margin-top: 50px;
    }
</style>

