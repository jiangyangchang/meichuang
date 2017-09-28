<template>
  <div class="content">
    <div class="title">美创的品牌力量</div>
    <ul class="list-content">
      <li class="list-item" v-for="item in content">
        <div class="border">
          <div class="img">
            <img :src="item.imgUrl" width="285" height="237" alt="">
          </div>
          <div class="name">{{item.name}}</div>
          <div class="text">{{item.text}}</div>
        </div>
      </li>
    </ul>
  </div>

</template>

<script type="text/ecmascript-6">
  export default{
    data() {
      return {
        content: [
          {
            'name': '数据安全',
            'imgUrl': 'http://www.mchz.com.cn/meichuang/src/images/index/pic-product-01.jpg',
            'text': '围绕核心数据保护，通过建立两个基础、管好三类资产、区分两类应用、管好三类人员，构建了由内而外的层层防御体系，' +
            '全方位构建敏感数据保护解决方案。'
          },
          {
            'name': '容灾备份',
            'imgUrl': 'http://www.mchz.com.cn/meichuang/src/images/index/pic-product-02.jpg',
            'text': '以业务系统为视角单元进行容灾建设； 以数据恢复、恢复管理为中心建设备份系统。'
          },
          {
            'name': '数据安全',
            'imgUrl': 'http://www.mchz.com.cn/meichuang/src/images/index/pic-product-03.jpg',
            'text': '遵循数据集成规范与标准，集成多样化数据，为不同机构提供数据开放和数据交换等应用，以及数据集成、治理、分析、决策等功能。'
          },
          {
            'name': 'IT维保服务',
            'imgUrl': 'http://www.mchz.com.cn/meichuang/src/images/index/pic-product-04.jpg',
            'text': 'ORACLE、IBM DB2、SQL SERVER, Mysql等数据库维保、Goldengate维保、 Weblogic维保。'
          }

        ]

      }
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .content
    width 1200px
    margin 0 auto
    .title
      width 100%
      height 86px
      line-height 86px
      font-size 36px
      font-weight bold
      text-align center
    .list-content
      display flex
      .list-item
        width 289px
        flex 1
        .border
          padding 2px 1px
          width 290px
          height 420px
          border solid 1px #cccccc
          .img
            margin-bottom 20px
            cursor pointer
          .name
            padding-left 15px
            margin-bottom 15px
            font-size 16px
            color #3366cc
            cursor pointer
          .text
            padding 0 15px
            font-size 14px
            line-height 20px
            cursor pointer
</style>
