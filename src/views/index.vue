<template>
  <div>
    <audio src="static/music/PG.mp3" loop autoplay="autoplay" controls preload="auto" style="position: absolute; left: -400px;"></audio>
  <header >
    <div class="wrap-header" style="background-image: url('static/loginBG.jpg')">
      <div class="main-header">
        <div class="zerogrid">
          <h1>Batherine</h1>
          <!-- <div class="counter">
            <div class="centered text-center" id="myCounter"></div>
          </div> -->
          <div class="countdown">
            <div class="countdown__days">
              <div class="number">{{countdownDays}}</div>
              <span class>天</span>
            </div>

            <div class="countdown__hours">
              <div class="number">{{countdownHours}}</div>
              <span class>小时</span>
            </div>

            <div class="countdown__minutes">
              <div class="number">{{countdownMinutes}}</div>
              <span class>分钟</span>
            </div>

            <div class="countdown__seconds">
              <div class="number">{{countdownSeconds}}</div>
              <span class>秒</span>
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
        <!-- <div class="zerogrid item1">
          <div class="row wrap-box" style="display: flex; justify-content: center;">
            <div class="box1">
              <div class="item1">
                <img src="static/images/pic11.jpg">
                <p></p>
              </div>
              <div class="text1">
                <p>第一次认识：<span @click="goCalendar('5.20')">2021.5.20</span></p>
                <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在一起：<span @click="goCalendar('6.1')">2021.6.1</span></p>
              </div>
              <div class="item1">
                <img src="static/images/pic12.jpg">
              </div>
            </div>
          </div>
        </div> -->
        <div class="container spacer-double-lg">
          <div class="row justify-content-center">
            <div class="col">
                <div class="mb-5 pb-5">
                  <!-- <h1 class="display-4 mb-0">最好的我们</h1> -->
                  <!-- <p class="w-md-40 mb-0 mx-auto text-dark-gray opacity-8 ">We are lucky to have them in our side</p> -->
                </div>
            </div>
          </div>
          <div class="row justify-content-center">
            <div class="col-md-4 d-flex flex-column align-items-center">
              <div class="px-5 mb-4 pb-4">
                <div class="svg-mask-container">
                  <!-- <svg width="100%" height="100%" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 980.2914 884.5557" enable-background="new 0 0 980.2914 884.5557" xml:space="preserve">
                      <defs>
                        <mask id="mask">
                            <path fill="#ffffff" d="M528.4855,192.3897L528.4855,192.3897C454.034,67.0629,292.3375,24.9363,166.115,98.3971
                              C38.8029,172.4928-3.0277,336.7236,71.1027,463.9358L286.945,834.3341c28.1165,48.2495,90.0233,64.5706,138.2729,36.4541
                              l368.4115-214.6845c127.2958-74.1792,172.7084-240.1479,98.7059-367.5465C818.4728,161.3996,655.4992,118.375,528.4855,192.3897z" />
                        </mask>
                      </defs>
                  </svg> -->
                    <img src="static/images/pic11.jpg" />
                </div>
                <div class="mt-4">
                    <h5 class="mb-0">雷䨻䨻</h5>
                    <!-- <span class="small">Bridesmaid </span> -->
                </div>
              </div>
            </div>
              <div class="col-md-4 d-flex flex-column align-items-center">
                <div class="px-5 mb-4 pb-4">
                  <div class="svg-mask-container">
                    <!-- <svg width="100%" height="100%" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0" y="0" viewBox="0 0 607 532" enable-background="new 0 0 607 532" xml:space="preserve">
                      <defs>
                        <mask id="mask-middle-2">
                            <path fill="#fff" d="M303.2954,55.7655L303.2954,55.7655c-68.9887-68.3032-180.269-68.3601-249.3155,0.1402
                              c-69.6423,69.0921-69.0838,181.9562,0.0139,251.5284l201.1888,202.5704c26.2076,26.3876,68.8445,26.5335,95.2321,0.3258
                              l368.4115-214.6845c127.2958-74.1792,172.7084-240.1479,98.7059-367.5465C818.4728,161.3996,655.4992,118.375,528.4855,192.3897z" />
                        </mask>
                        </defs>
                      <img mask="url(#mask-middle-2)" width="607" height="532" xlink:href="static/images/pic12.jpg"></img>
                    </svg> -->
                    <img src="static/images/pic12.jpg" />
                </div>
                <div class="mt-4">
                    <h5 class="mb-0">小猪丹宁</h5>
                    <!-- <span class="small">Groomsman </span> -->
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <section class="content-box boxstyle-1 box-1">
        <div class="row">
          <div class="col d-flex flex-column align-items-center">
              <ol class="story mb-0">
                <li>
                    <div class="story-icon bg-icon-primary">
                      <svg version="1.1" class="icon-svg" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 107 93" enable-background="new 0 0 107 93" xml:space="preserve">
                          <path fill="#E25D5D" d="M53.6825,9.4436L53.6825,9.4436C41.6532-2.4793,22.2392-2.5,10.1866,9.4439
                            c-12.1565,12.0471-12.07,31.7375-0.0219,43.8819l35.08,35.3601c4.5697,4.6061,12.0081,4.6357,16.6142,0.0661l35.1704-34.8918
                            c12.1523-12.056,12.4179-32.0464,0.3787-44.2154C85.3917-2.5013,65.8078-2.5857,53.6825,9.4436z"></path>
                      </svg>
                    </div>
                    <div>
                      <h5 class="mb-0">第一次相遇</h5>
                      <span class="small text-primary text1" @click="goCalendar('5.20')">2021-05-20</span>
                    </div>
                </li>
                <li>
                    <div class="story-icon bg-icon-primary">
                      <svg version="1.1" class="icon-svg" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 107 93" enable-background="new 0 0 107 93" xml:space="preserve">
                          <path fill="#E25D5D" d="M53.6825,9.4436L53.6825,9.4436C41.6532-2.4793,22.2392-2.5,10.1866,9.4439
                            c-12.1565,12.0471-12.07,31.7375-0.0219,43.8819l35.08,35.3601c4.5697,4.6061,12.0081,4.6357,16.6142,0.0661l35.1704-34.8918
                            c12.1523-12.056,12.4179-32.0464,0.3787-44.2154C85.3917-2.5013,65.8078-2.5857,53.6825,9.4436z"></path>
                      </svg>
                    </div>
                    <div>
                      <h5 class="mb-0">我们在一起了</h5>
                      <span class="small text-primary text1" @click="goCalendar('6.1')">2021-06-01</span>
                    </div>
                </li>
                <li>
                    <div class="story-icon bg-icon-primary">
                      <svg  version="1.1" class="icon-svg" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 107 93" enable-background="new 0 0 107 93" xml:space="preserve">
                          <path fill="#E25D5D" d="M53.6825,9.4436L53.6825,9.4436C41.6532-2.4793,22.2392-2.5,10.1866,9.4439
                            c-12.1565,12.0471-12.07,31.7375-0.0219,43.8819l35.08,35.3601c4.5697,4.6061,12.0081,4.6357,16.6142,0.0661l35.1704-34.8918
                            c12.1523-12.056,12.4179-32.0464,0.3787-44.2154C85.3917-2.5013,65.8078-2.5857,53.6825,9.4436z"></path>
                      </svg>
                    </div>
                    <div>
                      <h5 class="mb-0">相遇一周年</h5>
                      <span class="small text-primary">2022-05-20</span>
                    </div>
                </li>
                <li>
                    <div class="story-icon bg-icon-primary">
                      <svg  version="1.1" class="icon-svg" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 107 93" enable-background="new 0 0 107 93" xml:space="preserve">
                          <path fill="#E25D5D" d="M53.6825,9.4436L53.6825,9.4436C41.6532-2.4793,22.2392-2.5,10.1866,9.4439
                            c-12.1565,12.0471-12.07,31.7375-0.0219,43.8819l35.08,35.3601c4.5697,4.6061,12.0081,4.6357,16.6142,0.0661l35.1704-34.8918
                            c12.1523-12.056,12.4179-32.0464,0.3787-44.2154C85.3917-2.5013,65.8078-2.5857,53.6825,9.4436z"></path>
                      </svg>
                    </div>
                    <div>
                      <h5 class="mb-0">在一起一年啦</h5>
                      <span class="small text-primary">2022-06-01</span>
                    </div>
                </li>
              </ol>
          </div>
        </div>
        <div class="curved-decoration ">
            <svg width="100%" height="100%" class="bg-white-svg" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
              viewBox="0 0 2560 168.6227" enable-background="new 0 0 2560 168.6227" xml:space="preserve">
          <g>
          </g>
          <g>
            <path d="M2560,0c0,0-219.6543,165.951-730.788,124.0771c-383.3156-31.4028-827.2138-96.9514-1244.7139-96.9514
                c-212.5106,0-439,3.5-584.4982,1.5844l0,139.9126h2560V0z"></path>
          </g>
          </svg>
        </div>
      </section>
      <section class="content-box boxstyle-1 box-4">
        <div class="zerogrid">
          <div class="row wrap-box"><!--Start Box-->
            <div class="header">
              <div class="wrapper">
                <h2 class="color-yellow">Experience together</h2>
                <hr class="line">
              </div>
            </div>
            <div class="row"><!--Start Box-->
              <div class="col-1-3">
                <div class="wrap-col item">
                  <div class="zoom-container">
                    <img src="static/images/pic6.jpg" />
                  </div>
                  <div class="item-content">
                    <p>做一对属于我们的手机壳</p>
                  </div>
                </div>
              </div>
              <div class="col-1-3">
                <div class="wrap-col item">
                  <div class="zoom-container">
                    <img src="static/images/pic7.jpg" />
                  </div>
                  <div class="item-content">
                    <p>陪你做所有你想做的事</p>
                  </div>
                </div>
              </div>
              <div class="col-1-3">
                <div class="wrap-col item">
                  <div class="zoom-container">
                    <img src="static/images/pic8.jpg" />
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
                <h2 class="color-yellow">ALBUM</h2>
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
                  <img src="static/images/pic1.jpg" />
                </div>
              </div>
              <div class="col-1-3-2">
                <div class="item-container">
                  <div class="item-caption">
                    <div class="item-caption-inner">
                      <div class="item-caption-inner1"></div>
                    </div>
                  </div>
                  <img src="static/images/pic2.jpg" />
                </div>
              </div>
              <div class="col-1-3-2">
                <div class="item-container">
                  <div class="item-caption">
                    <div class="item-caption-inner">
                      <div class="item-caption-inner1"></div>
                    </div>
                  </div>
                  <img src="static/images/pic5.jpg" />
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
                  <img src="static/images/pic4.jpg" />
                </div>
              </div>
              <div class="col-1-3-2">
                <div class="item-container">
                  <div class="item-caption">
                    <div class="item-caption-inner">
                      <div class="item-caption-inner1"></div>
                    </div>
                  </div>
                  <img src="static/images/pic5.jpg" />
                </div>
              </div>
              <div class="col-1-3-2">
                <div class="item-container">
                  <div class="item-caption">
                    <div class="item-caption-inner">
                      <div class="item-caption-inner1"></div>
                    </div>
                  </div>
                  <img src="static/images/pic2.jpg" />
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
@import '../style/css22/main.css';
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
  justify-content: space-between;
  width: 50%;
}
.text1 {
  margin: 0 20px;
}
.text1{
  color: blueviolet;
  cursor: pointer;
  font-weight: 700;
}
.svg-mask-container {
  width: 200px;
  height: 200px;
  margin-bottom: 20px;
}
.svg-mask-container img{
  width: 100%;
  height: 100%;
  border-radius: 50%;
}
</style>
