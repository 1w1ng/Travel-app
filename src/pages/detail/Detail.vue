<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :list="list"></detail-list>
    </div>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      list: [{
        title: '促销票',
        children: [{
          title: '（促销）成人票（日夜场通玩）',
          children: [{
            title: '成人票(选定日期出游)',
          },{
            title: '（特惠）门票（日夜通用）',
          }]
        }]
      },{
        title: '成人票',
        children: [{
          title: '成人票（日场夜场通玩）',
          children: [{
            title: '成人门票（日场夜场通用 ）'
          }]
        },{
          title: '成人票（夜场）',
          children: [{
            title: '成人门票（夜场票）'
          }]
        }]
      }]
    }
  }
}
</script>

<style lang="scss" scoped>
  .content{
    height: 50rem;
  }
</style>
