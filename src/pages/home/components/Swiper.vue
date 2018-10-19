<template>
  <div class="wrapper">
    <swiper :options="swiperOption" >
    <!-- slides -->
    <swiper-slide v-for="item in swiperList" :key="item.id">
      <img class="swiper_img" :src="item.imgUrl" alt="">
    </swiper-slide>
    
    
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
    <div class="swiper-scrollbar"   slot="scrollbar"></div>
  </swiper>
  </div>
</template>

<script>
export default{
  name: 'HomeSwiper',
  data: function(){
    return{
      swiperOption: {
          // some swiper options/callbacks
          pagination:{
            el: '.swiper-pagination'
          }
      },
      swiperList: [{
        id: '1001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/ff/1bf7d3a4f6591002.jpg_750x200_40809f2a.jpg'
      },
      {
        id: '1002',
        imgUrl:'http://img1.qunarzz.com/piao/fusion/1809/2d/0d7dc3400a50b502.jpg_750x200_4ca95dd4.jpg'
      },
      {
        id: '1003',
        imgUrl:'http://img1.qunarzz.com/piao/fusion/1809/86/deb33800de224c02.jpg_750x200_74fb795e.jpg'
      }
      ]
    }
  }
}
</script>

<style scoped>
</style>
<style scoped> 
.swiper_img{
  width: 100%;
}
.wrapper >>> .swiper-pagination-bullet-active{
  background: #fff !important;
}
</style>


