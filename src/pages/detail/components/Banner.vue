<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1805/b2/b233a10ad2d39590a3.water.jpg_600x330_0d2a2d68.jpg" />
      <div class="banner-info">
        <div class="banner-title">
          世界之窗(AAAAA景区)
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe8ab;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    >
    </common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data(){
    return{
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1805/ed/edd6ad7136773cb1a3.water.jpg_r_800x800_e6277c27.jpg','http://img1.qunarzz.com/sight/p0/1608/32/32e98cce21e457dfa3.water.jpg_r_800x800_ce2c38c1.jpg','http://img1.qunarzz.com/sight/p0/1608/40/401f995038ca4d91a3.water.jpg_r_800x800_61120df4.jpg']
    }
  },
  methods: {
    handleBannerClick(){
      this.showGallary =  true
    },
    handleGallaryClose(){
      this.showGallary =  false
    }
  },
  components:{
    CommonGallary
  }
}
</script>

<style lang="scss" scoped>
  .banner{
    position: relative;
    overflow: hidden;
    height: 0;
    padding-bottom: 54%;
    .banner-img{
      width: 100%;
    }
    .banner-info{
      display: flex;
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      line-height: .6rem;
      color: #fff;
      background-image: linear-gradient(top , rgba(0,0,0,0) , rgba(0,0,0,0.8));
      .banner-title{
        flex: 1;
        font-size: .32rem;
        padding: 0 .2rem;
      }
      .banner-number{
        height: .32rem;
        line-height: .32rem;
        margin-top: .14rem;
        padding: 0 .4rem;
        border-radius: .2rem;
        background: rgba(0,0,0,.8);
        font-size: .24rem;
        .banner-icon{
          font-size: .24rem;
        }
      }
    }
  }
</style>