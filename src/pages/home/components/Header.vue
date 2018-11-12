<template>
<div class="header">
    <div class="header-left">
        <span class="iconfont">&#xe600;</span>
    </div>
    <div class="header-input">
        <span class="iconfont">&#xe68b;</span>
        输入城市景点</div>
    <div class="header-right">城市
        <span class="iconfont">&#xe8ed;</span>
    </div>
</div>
  
</template>
<script>
export default {};
</script>

<style lang='stylus' scoped> 
 @import '~styles/varibles.styl'
    .header
        text-align center
        line-height 0.86rem
        display flex
        height .86rem;
        color #fff
        background $bgColor
        .header-left
            width .64rem
            float left
            >span 
              padding .25rem  
        .header-input
            flex 1
            height 0.64rem
            line-height 0.64rem
            margin-top 0.12rem
            color #ccc
            text-align left
            margin-left .2rem
            background #fff
            border-radius .1rem
            >span 
                padding-left .2rem
        .header-right
            width 1.24rem
            float righ t  
            >span 
                font-size .1rem  
</style>
