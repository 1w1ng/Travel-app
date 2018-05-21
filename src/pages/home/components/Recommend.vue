<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data (){
    return {
      recommendList:[{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/ed/edd6ad7136773cb1a3.water.jpg_200x200_60b49263.jpg',
        title: '世界之窗',
        desc: '全球微缩景点，精彩演绎、娱乐项目应有尽有'
      },{
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_200x200_1c15c8f5.jpg',
        title: '深圳野生动物园',
        desc: '放养式动物园让你和动物们“零距离”'
      }]
    }
  }
}
</script>

<style lang="scss" scoped>
  .title{
    margin-top: .2rem;
    line-height: .8rem;
    background: #eee;
    text-indent: .2rem;
  }
  .item{
    overflow: hidden;
    display: flex;
    height: 1.9rem;
    .item-img{
      width: 1.7rem;
      height: 1.7rem;
      padding: .1rem;
    }
    .item-info{
      flex: 1;
      padding: .1rem;
      min-width: 0;
      .item-title{
        line-height: .54rem;
        font-size: .32rem;
      }
      .item-desc{
        line-height: .4rem;
        color: #ccc;
        font-size: .25rem;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
      }
      .item-button{
        line-height: .44rem;
        margin-top: .16rem;
        background: #ff9300;
        padding: 0 .2rem;
        border-radius: .06rem;
        color: #fff;
      }
    }
  }
</style>
