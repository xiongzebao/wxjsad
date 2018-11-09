<style type="text/css">
  .wxjs-img {
    width: 100%;
  }
  .title{
    font-weight: bold;
  }
  .desc{
    font-size: 0.25rem;
  }
</style>
<template>
  <div id='root'>
    <div v-for="(item,index) in list" v-bind:key="index">
      <h1 class="title">{{index+1}}、{{item.title}}</h1>
      <p class="desc">{{item.desc}}</p>
      <img class="wxjs-img" :src="item.imgUrl" />
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
        desc: "首页",
        title: "首页"
      })
      this.list.push({
        imgUrl: "../../../static/images/wxjsad/share2.jpg",
        desc: "统计页面",
        title: ""
      })
      this.list.push({
        imgUrl: "../../../static/images/wxjsad/share4.jpg",
        desc: "个人中心",
        title: ""
      })
      this.list.push({
        imgUrl: "../../../static/images/wxjsad/share5.jpg",
        desc: "",
        title: ""
      })
      this.list.push({
        imgUrl: "../../../static/images/wxjsad/share6.jpg",
        desc: "",
        title: ""
      })
      this.list.push({
        imgUrl: "../../../static/images/wxjsad/share7.jpg",
        desc: "",
        title: ""
      })
      this.list.push({
        imgUrl: "../../../static/images/wxjsad/wxjs_share_ad.png",
        desc: "",
        title: ""
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

