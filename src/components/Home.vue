<template>
  <div class="h-wrap">
    <video class="video" controls="controls" poster="http://si.geilicdn.com/resource-220b00000165465240420a02853e_750_422.jpg">
      <source src="../assets/common/info2.mp4" type="video/mp4">
    </video>
    <div class="bottom">
      <img src="//si.geilicdn.com/resource-12ca0000016557c0824f0a02853e-unadjust_750_915.png" width="100%" alt="">
      <div class="button" @click="toRegional">
        <span style="flex: auto;">杭州区域产业新城</span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .h-wrap {
    display: flex;
    flex-direction: column;
    .video {
      width: 100%;
      height: 210px;/*no*/
    }
    .h-tip {
      margin-left: 40px;
      margin-top: 40px;
      width: 200px;
      display: block;
    }
    .bottom {
      overflow: hidden;
      position: relative;
      .button {
        height: 100px;
        line-height: 100px;
        width: 406px;
        background-color: #bf0008;
        border-radius: 4px;/*no*/
        color: #ffffff;
        text-align: center;
        font-size: 18px;/*no*/
        position: absolute;
        top: 80%;
        left: 50%;
        transform: translate(-50%,-50%);
        z-index: 9;
        padding: 0 40px;
        display: flex;
        align-items: center;
        span {
          margin-right: 12px;
          &:after {
            content: "";
            width: 8px;/*no*/
            height: 8px;/*no*/
            border-right: 2px solid #ffffff;/*no*/
            border-bottom: 2px solid #ffffff;/*no*/
            transform: rotate(-45deg);
            position: absolute;
            top: 39%;
          }
        }
        
      }
    }
  }
</style>
<script>
  export default {
    name: 'Home',
    data() {
      return {
        show: true
      }
    },
    created() {
      document.body.scrollTop = 0
      document.documentElement.scrollTop = 0
    },
    methods: {
      toRegional() {
        this.$router.push({
          path: '/Regional'
        })
      },
      start() {
        this.show = false
      }
    }
  }
</script>