<template>
<div class="icons">
    <swiper>
       <swiper-slide v-for="(page,index) in pages" :key='index'>
          <div class="icon" v-for="list in page" :key = 'list.id'>
            <div class="icon-img">
            <img class="icon-img-content" :src="list.src" alt="">
            </div>
          <span class="icon-desc">我真的很长很长</span>
          </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  data(){
    return {
      lists:
        [{
          id:'001',
          src:'http://online.sccnn.com/img2/5890/coff160524-01.png'
        },{
           id:'001',
          src:'http://online.sccnn.com/img2/5890/coff160524-01.png'
        },{
           id:'001',
          src:'http://online.sccnn.com/img2/5890/coff160524-01.png'
        },{
           id:'001',
          src:'http://online.sccnn.com/img2/5890/coff160524-01.png'
        },{
          id:'001',
          src:'http://online.sccnn.com/img2/5890/coff160524-01.png'
        },{
          id:'001',
          src:'http://online.sccnn.com/img2/5890/coff160524-01.png'
        },{
           id:'001',
          src:'http://online.sccnn.com/img2/5890/coff160524-01.png'
        },{
           id:'001',
          src:'http://online.sccnn.com/img2/5890/coff160524-01.png'
        },{
          id:'001',
          src:'http://online.sccnn.com/img2/5890/coff160524-01.png'
        },{
           id:'001',
          src:'http://online.sccnn.com/img2/5890/coff160524-01.png'
        },{
          id:'001',
          src:'http://online.sccnn.com/img2/5890/coff160524-01.png'
        },]
    }
  },
  computed:{
    pages(){
      const pages = []
      this.lists.forEach((item,index)=>{
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
};
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import '~styles/mixins.styl';


.swiper-container{
  height: 0;
  padding-bottom: 50%;
  width 100%
}
.icons {
  overflow: hidden;
  height: 0;
  padding-bottom: 50%;
  width 100%
  /* 让高是宽的50% */

  .icon {
    float: left;
    text-align: center;
    height: 0;
    padding-bottom: 25%;
     /* 让高是父盒子高的50% */
    width: 25%;
    position: relative;

    .icon-img {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0.44 rem;
      box-sizing: border-box;
      padding: 0.1rem;
      /* .44rem是具体确定高度  改成边框盒子 加padding内压图片 */
      .icon-img-content {
        height: 100%;
        display: block;
        margin: 0 auto;
      /* 让盒子居中 100%改变图片大小去适合盒子的高度*/
      }
    }

    .icon-desc {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      line-height: 0.44rem;
      height: 0.44rem;
      color: $darkTextColor;
      ellipsis()
    }
  }
}
</style>
