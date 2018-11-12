<template>
<div class="swiper">
    <swiper :options="swiperOption">
        <swiper-slide v-for="item of swiperList" :key="item.id">
            <img :src='item.src'>
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
</div>
</template>

<script>
  export default {
    name: 'HomeSwiper',
    data() {
      return {
        swiperOption: {
            pagination: '.swiper-pagination',
            loop:true
        },
        swiperList:
            [{
                id:1,
                src:'https://imgs.qunarzz.com/vc/28/72/3d/07df240399f309da18e9a9854e.png_92.png'
            },{
                id:2,
                 src:'https://imgs.qunarzz.com/vc/42/26/bb/71d41bf5d04fcb589ece936cba.jpg_92.jpg'
            }]
      }
    },
  }
</script>

<style lang="stylus" scoped>
.swiper 
   width 100%
   height 31.25vw 
   background-color #ccc
   overflow hidden
   img 
       width 100%
       height 31.25vw

</style>
