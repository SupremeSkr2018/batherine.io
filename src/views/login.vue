<template>
  <div class="homepage-hero-module">
    <div class="video-container">
      <!-- <video :style="fixStyle" muted autoplay loop class="fillWidth" src="../assets/loginBG.mp4">
        浏览器不支持 video 标签，建议升级浏览器。
      </video> -->
      <svg height="320" width="320" id="aixin" class="like" @click="document.getElementById('#aixin').toggle('liked')">
          <path class="path" d="M 160 145 c 15 -90 170 -20 0 90 m 0 -90 c -15 -90 -170 -20 0 90" fill="gray"/>
        </svg>
      <img src="../assets/loginBG.jpg" alt="背景" style="width:100%;">
    </div>
  </div>
</template>

<script>
export default {
  name: 'login',
  data () {
    return {
      account: '',
      password: '',
      fixStyle: ''
    }
  },
  mounted () {

  },
  methods: {
    goIndex () {
      this.$router.push({
        name: 'index'
      })
    }
  }
}
</script>

<style>
canvas {
  position: absolute;
  width: 100%;
  height: 100%;
}
.el-header, .el-footer {
  background-color: #B3C0D1;
  color: #333;
  text-align: center;
  line-height: 60px;
}
.el-main {
  background-color: #E9EEF3;
  color: #333;
  text-align: center;
  line-height: 160px;
}
.homepage-hero-module,
  .video-container {
    position: relative;
    height: 100vh;
    overflow: hidden;
  }

  .video-container .poster img,
  .video-container video {
    z-index: 0;
    width: 100%;
    height: 100%;
    /* position: absolute; */
  }

  .video-container .filter {
    z-index: 1;
    position: absolute;
    background: rgba(0, 0, 0, 0.4);
  }
  .form{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: 0 auto;
    width: 400px;
    height: 200px;
  }
</style>
