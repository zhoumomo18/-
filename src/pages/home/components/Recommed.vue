<template>
    <div class="recommed border-bottom">
        <div class="recommed-img">
            <img src="http://img2.imgtn.bdimg.com/it/u=3445701240,1053655830&fm=15&gp=0.jpg" alt="">
        </div>
        <div class="recommed-context">
              <div class="recommed-title">
                   <p>我是超人</p>
               </div>
              <div class="recommed-text">
                  <p>我是超人我是超人</p>
               </div>
        </div>
      
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'

    .recommed
        display flex
        width 100%
        box-sizing border-box
        line-height 0.4rem
        padding .1rem
        .recommed-img
          width 2.5rem
          >img 
            width 2.5rem  
        .recommed-context
            flex 1
            min-width 0
            padding-left .1rem
            .recommed-text
                text-indent .2rem
                ellipsis()
</style>

