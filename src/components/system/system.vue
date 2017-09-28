<template>
  <div class="system">
    <div class="title">全面管理您的数据与系统</div>
    <ul class="system-list">
      <li v-for="item in system" class="system-item">
        <div class="avatar">
          <img :src="item.icon">
        </div>
        <div class="content">
          <div class="text">{{item.text}}</div>
          <div class="english">{{item.english}}</div>
        </div>
      </li>
    </ul>
  </div>

</template>

<script type="text/ecmascript-6">
  export default{
    data(){
      return {
        system: [
          {
            'icon': 'http://www.mchz.com.cn/meichuang/src/images/index/img-capaa.png',
            'text': '由内而外的多层防御保护机制',
            'english': 'TRUST CAPAA SYSTEM'
          },
          {
            'icon': 'http://www.mchz.com.cn/meichuang/src/images/index/img-data-integration.png',
            'text': '智能数据集成平台',
            'english': 'DATA INTEGRATION PLATFORM'
          },
          {
            'icon': 'http://www.mchz.com.cn/meichuang/src/images/index/img-dbra.png',
            'text': '保护业务系统的数据完整性和高可用性',
            'english': 'TRUST DBRA DISASTER/BACKUP SYSTEM'
          },
          {
            'icon': 'http://www.mchz.com.cn/meichuang/src/images/index/img-dbservice.png',
            'text': '数据库技术咨询与服务',
            'english': 'DATABASE SERVICE'
          }
        ]
      }
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .system
    width 1200px
    margin 0 auto
    padding 50px 100px
    .title
      margin-bottom 50px
      font-size 36px
      text-align center
      font-weight bold
    .system-list
      display flex
      flex-wrap wrap
      .system-item
        margin-bottom 50px
        width 500px
        font-size 0
        .avatar
          display inline-block
          margin-left 30px
          margin-right  30px
          vertical-align top
          cursor pointer
        .content
          display inline-block
          font-size 18px
          width 370px
          cursor pointer
</style>
