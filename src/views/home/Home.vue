<template>
    <div class="home-main">
        <div class="header-bar">
            <span class="search">

            </span>
            <p class="title">
                ZAOWU 造物
            </p>
            <a href="javascript:;" class="chat">

            </a>
            <a href="javascript:;" class="cart">
                
            </a>
        </div>
        <div class="swiper-section">
            <div class="swiper-title">
                <a @click="imgs = imgs1;"  href="javascript:;" class="swiper-title-link">推荐</a>
                <a @click="imgs = imgs2;" href="javascript:;" class="swiper-title-link">活动</a>
                <a href="javascript:;" class="swiper-title-link">品牌</a>
                <a href="javascript:;" class="swiper-title-link">定制</a>
            </div>
            <swiper class="swiper" :options="swiperOption" ref="mySwiper" @someSwiperEvent="callback">
                <!-- slides -->
                <swiper-slide v-for="(m,index) in imgs" :key="index">
                    <img :src="m.url" alt="">
                </swiper-slide>
            </swiper>
        </div>
        <monday-goods></monday-goods>
    </div>
    
</template>
<script>
import 'swiper/dist/css/swiper.css'

import { swiper, swiperSlide } from 'vue-awesome-swiper'
import MondayGoods from './components/MondayGoods'
export default {
    name: 'Home',
    components:{
        swiper,
        swiperSlide,
        MondayGoods
    },
    data() {
      return {
          imgs:[
              {
                  url:require('@assets/imgs/home/swiper-1.png')
              },
              {
                  url:require('@/assets/imgs/home/swiper-2.png')
              },
              {
                  url:require('@/assets/imgs/home/swiper-3.png')
              }

          ],
          imgs1:[
              {
                  url:require('@/assets/imgs/home/swiper-1.png')
              },
              {
                  url:require('@/assets/imgs/home/swiper-2.png')
              },
              {
                  url:require('@/assets/imgs/home/swiper-3.png')
              }

          ],
          imgs2:[
              
              {
                  url:require('@/assets/imgs/home/swiper-3.png')
              }

          ],
            swiperOption: {
                slidesPerView: 1.2,
                centeredSlides: true,
            }
      }
    },
    methods:{
        callback(){
        }
    }


}
</script>
<style lang="scss" scoped>
    .header-bar{
        position: fixed;
        left: 0;
        top: 0;
        width: 100%;
        height: 40px;
        background-color: #f5f5f5;
        z-index: 999;
        .search,.chat,.cart{
            position: absolute;
            left: 16px;
            top: 10px;
            width: 20px;
            height: 20px;
            background: url(../../assets/imgs/icons/search.png) no-repeat center;
            background-size: cover;
        }
        .title{
            font-size: 20px;
            color: #000;
            line-height: 40px;
            text-align: center;
            margin: 0 auto;
        }
        .chat{
            left: auto;
            right: 60px;
            background-image: url(../../assets/imgs/icons/chat.png);
        }
        .cart{
            left: auto;
            right: 20px;
            background-image: url(../../assets/imgs/icons/cart.png);
        }
    }
    .swiper-section{
        margin-top: 40px;
        width: 100%;
        height: 390px;
        overflow: hidden;
        .swiper-title{
            width: 100%;
            font-size: 15px;
            .swiper-title-link{
                color: #010E0D;
                text-decoration: none;
                padding: 0 16px;
                border-right: 1px solid #f5f5f5;
                &:last-child{
                    border-right: none;
                }
            }
            margin: 20px auto;
        }
        .swiper{
            width: 100%;
            height: 100%;
        }
    }
    .monday-goods{
        width: 100%;
        height: 500px;
        margin-top: 200px;
        background-color: pink;
    }
</style>


