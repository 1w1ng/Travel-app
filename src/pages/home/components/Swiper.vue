<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id" data-swiper-autoplay="3000">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>


<script>
export default{
  name: 'HomeSwiper',
  data (){
    return{
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: true
      },
      swiperList:[{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/77/f63bd04dd5319602.jpg_750x200_6ba8e0ca.jpg'
      },{
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/e5/59fad13a64807d02.jpg_750x200_713ae984.jpg'
      },{
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/f2/91b285a08ee21c02.jpg_750x200_8a73fd08.jpg'
      },{
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/a8/c49ed2bbbdbce402.jpg_750x200_818d911d.jpg'
      },{
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/d3/b7a5b50ae4303802.jpg_750x200_c4f83b96.jpg'
      },{
        id: '0006',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/3e/4d6e12949f74fc02.jpg_750x200_22aba1bb.jpg'
      },{
        id: '0007',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1708/7c/c0b9acba07764302.jpg_750x200_389436b7.jpg'
      },{
        id: '0008',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/ff/86d79cd397cbe802.jpg_750x200_41ce1524.jpg'
      },{
        id: '0009',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/85/ed01cd5307b3f602.jpg_750x200_e54ef754.jpg'
      }]
    }
  }
}
</script>


<style>
  .swiper-pagination-bullet-active{
    background: #fff !important;
  }
</style>


<style lang="scss" scoped>
  .wrapper{
    overflow: hidden;
    width: 100%;
    height: 0;
    padding-bottom: 26.6%;
    background: #eee;
    .swiper-img{
      width: 100%;
    }
  }
</style>
