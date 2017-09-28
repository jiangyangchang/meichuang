<template>
  <div id="app">
    <v-header></v-header>
    <v-carousel></v-carousel>
    <v-content></v-content>
    <v-carousel2></v-carousel2>
    <v-system></v-system>
    <v-carousel3></v-carousel3>
    <v-footer></v-footer>
    <div class="consult">
      <span class="text" @click="toggleMessage">在线咨询</span>
    </div>
    <div class="message" v-show="messageShow" ref="content">
      <div class="title">
        <span class="text">请您留言</span>
        <span class="glyphicon glyphicon-minus" aria-hidden="true" @click="foldMessage" v-show="unfold"></span>
        <span class="glyphicon glyphicon-unchecked" aria-hidden="true" @click="unfoldMessage" v-show="fold"></span>
      </div>
      <form class="toggle-content" ref="message">
        <textarea placeholder="请在此输入留言内容，我们会尽快您联系" rows="4" cols="28" class="message-content"></textarea>
        <div class="name">
          <span class="glyphicon glyphicon-user" aria-hidden="true"></span>
          <input placeholder="姓名">
        </div>
        <div class="telephone">
          <span class="glyphicon glyphicon-earphone" aria-hidden="true"></span>
          <input placeholder="电话（必填）">
        </div>
        <div class="email">
          <span class="glyphicon glyphicon-envelope" aria-hidden="true"></span>
          <input placeholder="邮箱">
        </div>
        <div class="adress">
          <span class="glyphicon glyphicon-home" aria-hidden="true"></span>
          <input placeholder="地址">
        </div>
        <input type="submit" class="btn btn-danger dropdown-toggle">
      </form>
    </div>
  </div>
</template>

<script>
  import header from './components/header/header.vue'
  import carousel from './components/carousel/carousel.vue'
  import content from './components/content/content.vue'
  import carsousel2 from './components/carsousel2/carsousel2.vue'
  import system from './components/system/system.vue'
  import carsousel3 from './components/carsousel3/carsousel3.vue'
  import footer from './components/footer/footer.vue'
  export default {
    name: 'app',
    data(){
      return {
        messageShow: false,
        unfold: true,
      }
    },
    methods: {
      toggleMessage(){
        this.messageShow = true;
        this.unfold=true;
        this.$refs.message.style.display = 'block';
        this.$refs.content.style.bottom = 50 + '%';
        this.$refs.content.style.left = 50 + '%';
        this.$refs.content.style.marginBottom = -175 + 'px';
        this.$refs.content.style.marginLeft = -120 + 'px';
      },
      foldMessage(){
        this.unfold = !this.unfold;
        this.$refs.message.style.display = 'none';
        this.$refs.content.style.margin = 0 + 'px';
        this.$refs.content.style.bottom = 0 + 'px';
        this.$refs.content.style.left = 0 + 'px';

      },
      unfoldMessage(){
        this.unfold = !this.unfold;
        this.$refs.message.style.display = 'block'
      }
    },
    computed: {
      fold(){
        return !this.unfold
      }
    },
    components: {
      'v-header': header,
      'v-carousel': carousel,
      'v-content': content,
      'v-carousel2': carsousel2,
      'v-system': system,
      'v-carousel3': carsousel3,
      'v-footer': footer
    }

  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .consult
    position fixed
    right 15px
    bottom 30px
    width 140px
    line-height 56px
    height 56px
    text-align center
    background #00aef3
    cursor pointer
    .text
      font-size 26px
      font-weight bolder
      color #ffffff

  .message
    position fixed
    bottom 50%
    left 50%
    margin-bottom -175px
    margin-left -120px
    width 240px

    background #cccccc
    z-index 100
    .title
      height 35px
      line-height 35px
      background #00aef3
      .text
        color #ffffff
        margin-left 10px
      .glyphicon
        color #ffffff
        float right
        line-height 35px
        margin-right 15px
    .message-content
      width 220px
      margin 10px 0 5px 10px
    .name, .telephone, .email, .adress
      margin 10px 10px
      width 220px
      background #ffffff
      font-size 14px
      height 22px
      line-height 22px
      .glyphicon
        margin 0 5px
      input
        width 150px
        height 20px
    .btn
      margin-left 10px
      margin-bottom 10px
</style>
