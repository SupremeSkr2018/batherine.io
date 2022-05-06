<template>
  <div>
    <audio src="/static/music/PG.mp3" loop autoplay="autoplay" controls preload="auto" style="position: absolute; left: -400px;"></audio>
  <header >
    <div class="wrap-header">
      <div class="main-header">
        <div class="zerogrid">
          <h1>Batherine</h1>
          <!-- <div class="counter">
            <div class="centered text-center" id="myCounter"></div>
          </div> -->
          <div class="countdown">
            <div class="countdown__days">
              <div class="number">{{countdownDays}}</div>
              <span class>Days</span>
            </div>

            <div class="countdown__hours">
              <div class="number">{{countdownHours}}</div>
              <span class>Hours</span>
            </div>

            <div class="countdown__minutes">
              <div class="number">{{countdownMinutes}}</div>
              <span class>Minutes</span>
            </div>

            <div class="countdown__seconds">
              <div class="number">{{countdownSeconds}}</div>
              <span class>Seconds</span>
            </div>
          </div>
          <div>

          </div>
        </div>
      </div>
    </div>
  </header>
  <section id="container">
    <div class="wrap-container">
      <!-----------------content-box-1-------------------->
      <section class="content-box boxstyle-1 box-1">
        <div class="zerogrid item1">
          <div class="row wrap-box"><!--Start Box-->
            <div class="box1">
              <div class="item1">
                <img src="@/assets/images/pic11.jpg">
              </div>
              <div class="text1">
                <p>第一次认识：<span @click="goCalendar('5.20')">2021.5.20</span></p>
                <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在一起：<span @click="goCalendar('6.1')">2021.6.1</span></p>
              </div>
              <div class="item1">
                <img src="@/assets/images/pic12.jpg">
              </div>
            </div>
          </div>
        </div>
      </section>
      <section class="content-box boxstyle-1 box-4">
        <div class="zerogrid">
          <div class="row wrap-box"><!--Start Box-->
            <div class="header">
              <div class="wrapper">
                <h2 class="color-yellow">OUR BLOG</h2>
                <hr class="line">
              </div>
            </div>
            <div class="row"><!--Start Box-->
              <div class="col-1-3">
                <div class="wrap-col item">
                  <div class="zoom-container">
                    <img src="../assets/images/pic6.jpg" />
                  </div>
                  <div class="item-content">
                    <p>做一对属于我们的手机壳</p>
                  </div>
                </div>
              </div>
              <div class="col-1-3">
                <div class="wrap-col item">
                  <div class="zoom-container">
                    <img src="../assets/images/pic7.jpg" />
                  </div>
                  <div class="item-content">
                    <p>陪你做所有你想做的事</p>
                  </div>
                </div>
              </div>
              <div class="col-1-3">
                <div class="wrap-col item">
                  <div class="zoom-container">
                    <img src="../assets/images/pic8.jpg" />
                  </div>
                  <div class="item-content">
                    <p>守着夕阳西下，给你讲永远好笑的笑话</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <section class="content-box boxstyle-2 box-2">
        <div class="zerogrid" style="width: 100%;">
          <div class="row row2 wrap-box"><!--Start Box-->
            <div class="header">
              <div class="wrapper">
                <h2 class="color-yellow">GALLERY</h2>
                <hr class="line">
              </div>
            </div>
            <div class="row row2">
              <div class="col-1-3-2">
                <div class="item-container">
                  <div class="item-caption">
                    <div class="item-caption-inner">
                      <div class="item-caption-inner1"></div>
                    </div>
                  </div>
                  <img src="../assets/images/pic1.jpg" />
                </div>
              </div>
              <div class="col-1-3-2">
                <div class="item-container">
                  <div class="item-caption">
                    <div class="item-caption-inner">
                      <div class="item-caption-inner1"></div>
                    </div>
                  </div>
                  <img src="../assets/images/pic2.jpg" />
                </div>
              </div>
              <div class="col-1-3-2">
                <div class="item-container">
                  <div class="item-caption">
                    <div class="item-caption-inner">
                      <div class="item-caption-inner1"></div>
                    </div>
                  </div>
                  <img src="../assets/images/pic5.jpg" />
                </div>
              </div>
            </div>
            <div class="row row2">
              <div class="col-1-3-2">
                <div class="item-container">
                  <div class="item-caption">
                    <div class="item-caption-inner">
                      <div class="item-caption-inner1"></div>
                    </div>
                  </div>
                  <img src="../assets/images/pic4.jpg" />
                </div>
              </div>
              <div class="col-1-3-2">
                <div class="item-container">
                  <div class="item-caption">
                    <div class="item-caption-inner">
                      <div class="item-caption-inner1"></div>
                    </div>
                  </div>
                  <img src="../assets/images/pic5.jpg" />
                </div>
              </div>
              <div class="col-1-3-2">
                <div class="item-container">
                  <div class="item-caption">
                    <div class="item-caption-inner">
                      <div class="item-caption-inner1"></div>
                    </div>
                  </div>
                  <img src="../assets/images/pic2.jpg" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </section>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      countdownDays: '00',
      countdownHours: '00',
      countdownMinutes: '00',
      countdownSeconds: '00'
    }
  },
  created () {
    const deadlineDate = new Date('May 20, 2021 20:00:00').getTime()
    setInterval(() => {
      const currentDate = new Date().getTime()
      const distance = currentDate - deadlineDate
      const days = Math.floor(distance / (1000 * 60 * 60 * 24))
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60))
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60))
      const seconds = Math.floor((distance % (1000 * 60)) / 1000)
      this.countdownDays = days
      this.countdownHours = hours
      this.countdownMinutes = minutes
      this.countdownSeconds = seconds
    }, 1000)
  },
  methods: {
    goCalendar (day) {
      this.$router.push({
        name: 'calendar',
        params: {
          day
        }
      })
    }
  }
}
</script>
<style>
@import '../style/font-awesome/css/font-awesome.min.css';
@import '../style/mb-comingsoon-iceberg.css';
@import '../style/zerostyle.css';
@import '../style/zerogrid.css';
@import '../style/index.scss';
@import '../style/timeCard/css/font-awesome.min.css';
@import '../style/timeCard/css/style.css';
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
.countdown{
  margin: auto;
  display: table;
  font-size: 28px;
  font-weight: 500;
}
.countdown>div{
  float: left;
  min-width: 100px;
  margin: 40px 10px 0px 0px;
  font-size: 60px;
  font-weight: 700;
  color: #fff;
  background: rgb(35 1 1 / 21%);
  border-radius: 6px;
  padding: 20px 14px;
}
.countdown span{
  position: relative;
  display: block;
  font-size: 12px;
  text-align: center;
  text-transform: uppercase;
  font-weight: 600;
  letter-spacing: 1px;
  color: #ffba08;
  top: 20px;
}
</style>
<style lang="css">
.item1 img {
  width: 200px !important;
  height: 200px !important;
}
.box1{
  display: flex;
  align-items: center;
  justify-content: center;
}
.text1 {
  margin: 0 20px;
}
.text1 span{
  color: blueviolet;
  cursor: pointer;
  font-weight: 700;
}
</style>
