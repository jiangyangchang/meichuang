<template>
  <div class="footer-wrapper">
    <div class="footer-top">
      <div class="footer-left">
        <ul class="left-content">
          <li class="left-list">
            <div class="title">产品</div>
            <ul>
              <li class="inner-list">数据安全</li>
              <li class="inner-list">容灾备份</li>
              <li class="inner-list">大数据</li>
              <li class="inner-list">IT维保服务</li>
            </ul>
          </li>
          <li class="left-list">
            <div class="title">常用信息</div>
            <ul>
              <li class="inner-list">关于美创</li>
              <li class="inner-list">加入美创</li>
              <li class="inner-list">年度培训</li>
            </ul>
          </li>
          <li class="left-list">
            <div class="title">美创社区</div>
            <ul>
              <li class="inner-list">技术博客</li>
              <li class="inner-list">新闻资讯</li>
              <li class="inner-list">大咖课堂</li>
            </ul>
          </li>
          <li class="left-list">
            <div class="title">联系美创</div>
            <ul>
              <li class="inner-list">分支机构</li>
            </ul>
          </li>
        </ul>
      </div>
      <div class="footer-right">
        <div class="right-content">
          <div class="inner">
            <span class="glyphicon glyphicon-picture" aria-hidden="true"></span>
            <span class="text">美创订阅号</span>
            <img src="http://www.mchz.com.cn/meichuang/src/images/common/service.png">
          </div>
          <div class="inner">
            <span class="glyphicon glyphicon-picture" aria-hidden="true"></span>
            <span class="text">美创服务号</span>
            <img src="http://www.mchz.com.cn/meichuang/src/images/common/subscribe.png">
          </div>
          <div class="telephone">
            <span class="glyphicon glyphicon-phone" aria-hidden="true"></span>
            <span class="number">400-711-8011</span>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <img src="http://www.mchz.com.cn/meichuang/src/images/common/net-security.gif">
      <span class="text">版权所有 杭州美创科技有限公司 Copyright 2005-2016,All rights reserverd. 浙ICP备 09009762号-1</span>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">

</script>

<style lang="stylus" rel="stylesheet/stylus">
  .footer-wrapper
    width 100%
    background black
    color #ffffff
    .footer-top
      padding 50px 0
      width 1200px
      margin 0 auto
      .footer-left
        display inline-block
        width 880px
        .left-content
          display inline-block
          .left-list
            display inline-block
            vertical-align top
            padding 0 10px
            width 200px
            height 160px
            .title
              font-size 26px
              margin-bottom 30px
              cursor pointer
            .inner-list
              font-size 16px
              line-height 26px
      .footer-right
        display inline-block
        vertical-align top
        width 300px
        .right-content
          .inner
            display inline-block
            width 140px
            .glyphicon
              margin-right 5px
            img
              margin-top 15px
              cursor pointer
          .telephone
            width 300px
            margin-top 25px
            margin-left 30px
            font-size 26px
            cursor pointer

    .footer-bottom
      border-top solid #cccccc 1px
      text-align center
      padding 20px 0
      img
        width 52px
        height 56px
        cursor pointer
      .text
        cursor pointer


</style>
