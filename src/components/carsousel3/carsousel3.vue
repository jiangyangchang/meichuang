<template>
  <div class="content-wrapper">
    <div class="contentB">
      <div class="content-left">
        <span class="glyphicon glyphicon-chevron-left" @click="slidePre" aria-hidden="true"></span>
        <span class="glyphicon glyphicon-chevron-right" @click="slideNext" aria-hidden="true"></span>
        <transition-group name="fade">
          <div class="slide-content" v-show="index===nowPage" v-for="(item,index) in banners" key="index">
            <img :src="item.sourceUrl" width="300" height="300">
            <div class="article">
              <div class="name">{{item.title}}</div>
              <div class="time">{{item.time}}</div>
              <div class="text">{{item.text}}</div>
            </div>
          </div>
        </transition-group>
      </div>
      <div class="content-right">
        <ul>
          <li v-for="item in news" class="news-item">
            <span class="news-name">{{item.newsName}}</span>
            <span class="time">{{item.time}}</span>
            <span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span>
          </li>
        </ul>
        <div class="showmore">查看更多</div>
      </div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default{
    data(){
      return {
        banners: [
          {
            'title': '分享Oracle 12C新特性，步入数据库云时代',
            'time': '2017-05-22 11:09:29',
            'text': 'Oracle 12.1已推出多年，更稳定、更先进的12.2也于今年3月正式发布。美创科技敏锐感知用户需求，在年初就成立了Oracle 12C技术专题组，并投入10余名数据库专家，针对Oracle 12C新特性进行了系统性研究。',
            'sourceUrl': 'http://www.mchz.com.cn/mc/attach/ckfinder/userfiles/2017-05-22images/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20170518110910.jpg'
          },
          {
            'title': '《网络安全法》系列之二：个人信息，如何织密“保护网”?',
            'time': '2017-05-22 11:02:42',
            'text': '如果不曾遭遇，你永远不知道，个人信息泄露有多“可怕”。个人信息泄露是网络诈骗泛滥的重要原因，今年以来，舆论关注的山东两名大学生遭电信诈骗死亡案、清华大学教授遭电信诈骗案，皆因个人信息泄露之后',
            'sourceUrl': 'http://www.mchz.com.cn/mc/attach/ckfinder/userfiles/2017-05-22images/3.jpg'
          },
          {
            'title': '分享Oracle 12C新特性，步入数据库云时代',
            'time': '2017-05-22 11:09:29',
            'text': 'Oracle 12.1已推出多年，更稳定、更先进的12.2也于今年3月正式发布。美创科技敏锐感知用户需求，在年初就成立了Oracle 12C技术专题组，并投入10余名数据库专家，针对Oracle 12C新特性进行了系统性研究。',
            'sourceUrl': 'http://www.mchz.com.cn/mc/attach/ckfinder/userfiles/2017-05-22images/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20170518110910.jpg'
          },
          {
            'title': '《网络安全法》系列之二：个人信息，如何织密“保护网”?',
            'time': '2017-05-22 11:02:42',
            'text': '如果不曾遭遇，你永远不知道，个人信息泄露有多“可怕”。个人信息泄露是网络诈骗泛滥的重要原因，今年以来，舆论关注的山东两名大学生遭电信诈骗死亡案、清华大学教授遭电信诈骗案，皆因个人信息泄露之后',
            'sourceUrl': 'http://www.mchz.com.cn/mc/attach/ckfinder/userfiles/2017-05-22images/3.jpg'
          }
        ],
        nowPage: 0,
        news:[
          {'newsName':'sudo用户免密输入设置','time':'2017-05-11'},
          {'newsName':'sudo用户免密输入设置','time':'2017-05-11'},
          {'newsName':'sudo用户免密输入设置','time':'2017-05-11'},
          {'newsName':'sudo用户免密输入设置','time':'2017-05-11'},
          {'newsName':'sudo用户免密输入设置','time':'2017-05-11'},
          {'newsName':'sudo用户免密输入设置','time':'2017-05-11'}
        ]
      }
    },
    created(){
      this.autoSlide()
    },
    methods: {
      slideNext () {
        const lastPage = this.banners.length - 1;
        if (this.nowPage < lastPage) {
          this.nowPage += 1
        } else {
          this.nowPage = 0
        }
      },
      slidePre () {
        const lastPage = this.banners.length - 1;
        if (this.nowPage > 0) {
          this.nowPage -= 1
        } else {
          this.nowPage = lastPage
        }
      },
      autoSlide () {
        clearInterval(this.prevTid);
        this.prevTid = setInterval(() => {
          this.slideNext()
        }, 5000)
      }
    }

  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .content-wrapper
    width 100%
    background #ececec
    .contentB
      width 1200px
      margin 0 auto
      position relative
      .content-left
        position relative
        width 770px
        height 380px
        padding 30px 0
        .glyphicon
          font-size 40px
          position absolute
          z-index 10
          display block
          width 40px
          height 40px
          cursor pointer
          &:hover
            color red
        .glyphicon-chevron-left
          top 160px
        .glyphicon-chevron-right
          top 160px
          right 0
        .slide-content
          position absolute
          top 20px
          left 30px
          padding 20px
          font-size 0
          opacity 1
          z-index 1
          img
            display inline-block
            margin-right 30px
            vertical-align top
            cursor pointer
          .article
            display inline-block
            width 350px
            .name
              font-size 20px
              margin-bottom 20px
              cursor pointer
            .time
              font-size 12px
              margin-bottom 20px
              padding-bottom 10px
              line-height 20px
              border-bottom solid black 1px
            .text
              font-size 16px
              cursor pointer

          &.fade-leave-active,&.fade-enter-active
            transition all 0.5s
          &.fade-enter,&.fade-leave-active
            opacity 0
      .content-right
        position absolute
        top 40px
        right 0
        width 400px
        .news-item
          height 40px
          line-height 40px
          cursor pointer
          &:hover
            color #1b6d85
          .news-name
            display inline-block
            width 250px
          .time
            margin-right 20px



        .showmore
          float right
          margin-right 50px
          &:hover
            color red
            font-size 16px
            cursor pointer
</style>
