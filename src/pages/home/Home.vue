<template>
<div>
   <home-header></home-header>   
   <home-swiper></home-swiper>
   <home-icons></home-icons>
   <home-recommed></home-recommed>
</div>
</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommed from './components/Recommed'

export default {
    name:'Home',
    components:{
        HomeHeader,
        HomeSwiper,
        HomeIcons,
        HomeRecommed
    }
}
</script>
<style>

</style>


