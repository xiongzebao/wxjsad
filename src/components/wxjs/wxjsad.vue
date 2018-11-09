<style type="text/css">
  .wxjs-img {
    width: 100%;
    margin-top: 0.1rem;
  }
  .title {
    font-weight: bold;
    margin-top:0.1rem;
  }
  .desc {
    font-size: 0.3rem;
     letter-spacing:3px;
     line-height: 0.5rem;
  }
  .text {
    display: flex;
    flex-direction: column;
  }
  #root{
    padding: 0.1rem;
  }
</style>
<template>
  <div id='root'>
    <div v-for="(item,index) in list" v-bind:key="index">
      <h1 class="title">{{index+1}}、{{item.title}}</h1>
      <img class="wxjs-img" :src="item.imgUrl" />
      <div class="text">
        <p class="desc">{{item.desc}}</p>
      </div>
    </div>
  </div>
</template>


<script>
  import Vue from 'vue'
  import {
    MessageBox
  } from 'mint-ui';
  export default {
    name: 'app',
    beforeCreated() {},
    mounted() {
      this.list.push({
        imgUrl: "../../../static/images/wxjsad/share1.jpg",
        title: "首页",
        desc: ` 首页以圆形容器很非常形象真实的展示了你最近两个月身体的精气状况，这些数值是通过你的打卡数据通过科学地算法统计出来的，
              当数据显示异常（精气不足，偏低时）说明你已经纵欲过度，每次打卡完成积累2ml精气，未完成卸掉5毫升精气，当人体低于60毫升精气值时表示精气不足
              首页标签显示根据你的签到状况和大数据统计给予温馨提醒和建议等，请务必要每天签到，否则数据不完整会导致统计结果不不准确，影响数据的客观真实性。
              `
      })
      this.list.push({
        imgUrl: "../../../static/images/wxjsad/share2.jpg",
        desc: "统计页面统计了你每个月的签到情况，可以直观地查看每个月每天签到是否完成，点击当前或最近三天可以打卡或补卡，也可以在下方查看签到心得",
        title: "统计页面"
      })
      this.list.push({
        imgUrl: "../../../static/images/wxjsad/share4.jpg",
        desc: "个人中心可以修改头像昵称，以及进入各个功能模块",
        title: "个人中心"
      })
      // this.list.push({
      //   imgUrl: "../../../static/images/wxjsad/share5.jpg",
      //   desc: "持戒记录，详细的统计了你的签到情况",
      //   title: "持戒记录"
      // })
      this.list.push({
        imgUrl: "../../../static/images/wxjsad/share6.jpg",
          desc: "显示签到超过一周的圈友，按签到天数排序",
        title: "圈友"
      })
      this.list.push({
        imgUrl: "../../../static/images/wxjsad/share7.jpg",
        desc: "任何圈友都可在此留言",
        title: "留言板"
      })
      this.list.push({
        imgUrl: "../../../static/images/wxjsad/wxjs_share_ad.png",
        desc: "微信搜索小程序:戒色圈，成为圈友",
        title: "加入戒色圈"
      })
    },
    computed: {},
    data() {
      return {
        list: []
      }
    },
    methods: {},
    components: {}
  }
</script>

