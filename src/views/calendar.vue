<template>
  <div>
    <audio src="static/music/doushini.mp3" loop autoplay="autoplay" controls preload="auto" style="position: absolute; left: -400px;"></audio>
    <canvas id="canvas"></canvas>
    <div v-if="day == '5.20'">
      <div class="A">
        <img src="static/images/pic13.jpg" alt="">
        <img src="static/images/pic14.jpg" alt="">
      </div>
      <div style="position: absolute;top: 155px;right: 550px;z-index: 999;color: #ff6f00;">
        <p style="fontSize: 20px;margin-bottom: 10px;">今天第一次见到我的女孩，没有想到后来会那么爱她！</p>
        <span style="fontSize: 15px;">因为我不想加班跑去凑热闹<br>你是陪着朋友去帮她追到她的男孩 <br>
        机缘巧合的认识了你 <br>我现在很感谢那个主持人把我带到你旁边！</span>
      </div>
    </div>
    
    <div v-else>
      <div class="B">
        <img src="static/images/pic3.jpg" alt="">
        <img src="static/images/pic15.jpg" alt="">
        <img src="static/images/pic16.jpg" alt="">
      </div>
      <div style="position: absolute;top: 155px;right: 550px;z-index: 999;color: #ff6f00;">
        <p style="fontSize: 20px;margin-bottom: 10px;">今天和我最爱的女孩在一起啦！！！</p>
        <span style="fontSize: 15px;">我的女孩每天去接我下班，然后一起在公司园区散步，讲着自己的故事</span>
      </div>
    </div>
    <div v-if="day == '5.20'" class="main-container">
      <div class="calendar-head">
        <h4 class="current-weekday">20号 星期四</h4>
        <h4 class="month-year">2021 5月</h4>
      </div>
      <div class="calendar-body">
        <ul class="weekdays">
          <li>一</li>
          <li>二</li>
          <li>三</li>
          <li>四</li>
          <li>五</li>
          <li>六</li>
          <li>日</li>
        </ul>

        <ul class="days">
          <li class="previous-month">26</li>
          <li class="previous-month">27</li>
          <li class="previous-month">28</li>
          <li class="previous-month">29</li>
          <li class="previous-month">30</li>
          <li>1</li>
          <li>2</li>
          <li>3</li>
          <li>4</li>
          <li>5</li>
          <li>6</li>
          <li>7</li>
          <li>8</li>
          <li>9</li>
          <li>10</li>
          <li>11</li>
          <li>12</li>
          <li>13</li>
          <li>14</li>
          <li>15</li>
          <li>16</li>
          <li>17</li>
          <li>18</li>
          <li>19</li>
          <li><span class="active"></span><span class="active_text">20</span></li>
          <li>21</li>
          <li>22</li>
          <li>23</li>
          <li>24</li>
          <li>25</li>
          <li>26</li>
          <li>27</li>
          <li>28</li>
          <li>29</li>
          <li>30</li>
          <li>31</li>
        </ul>
      </div>
    </div>
    <div v-else class="main-container">
      <div class="calendar-head">
        <h4 class="current-weekday">1号 星期二</h4>
        <h4 class="month-year">2021 6月</h4>
      </div>
      <div class="calendar-body">
        <ul class="weekdays">
          <li>一</li>
          <li>二</li>
          <li>三</li>
          <li>四</li>
          <li>五</li>
          <li>六</li>
          <li>日</li>
        </ul>

        <ul class="days">
          <li class="previous-month">31</li>
          <li><span class="active active2"></span><span class="active_text">1</span></li>
          <li>2</li>
          <li>3</li>
          <li>4</li>
          <li>5</li>
          <li>6</li>
          <li>7</li>
          <li>8</li>
          <li>9</li>
          <li>10</li>
          <li>11</li>
          <li>12</li>
          <li>13</li>
          <li>14</li>
          <li>15</li>
          <li>16</li>
          <li>17</li>
          <li>18</li>
          <li>19</li>
          <li>20</li>
          <li>21</li>
          <li>22</li>
          <li>23</li>
          <li>24</li>
          <li>25</li>
          <li>26</li>
          <li>27</li>
          <li>28</li>
          <li>29</li>
          <li>30</li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: '',
  data () {
    return {
      day: ''
    }
  },
  created () {
    this.day = this.$route.params.day
  },
  mounted () {
    this.load()
  },
  methods: {
    load() {
      let canvas = document.getElementById('canvas');
    //   if (!canvas || !canvas.getContext) {
    //   return false;
    // }
    function rand(min, max) {
      return Math.floor(Math.random() * (max - min + 1) + min);
    }
    let ctx = canvas.getContext('2d');
    let X = canvas.width = window.innerWidth;
    let Y = canvas.height = window.innerHeight;
    let mouseX = null;
    let mouseY = null;
    let bubbles = [];
    let bubbleNum = 150;
    let shapes = [];
    let rad = Math.PI * 2 / 4;
    let style = {
      black: 'black',
      white: 'white',
      lineWidth: 4,
    };

    if (X < 768) {
      bubbleNum = 100;
    }
    window.requestAnimationFrame =
      window.requestAnimationFrame ||
      window.mozRequestAnimationFrame ||
      window.webkitRequestAnimationFrame ||
      window.msRequestAnimationFrame ||
      function(cb) {
        setTimeout(cb, 17);
      };
    function Bubble(ctx, x, y) {
      this.ctx = ctx;
      this.init(x, y);
    }
    Bubble.prototype.init = function(x, y) {
      this.x = x;
      this.y = y;
      this.r = rand(20, 50);
      this.ga = Math.random() * Math.random() * Math.random();
      this.v = {
        x: rand(-1, 1) * Math.random() * Math.random(),
        y: Math.random()
      };
      this.random = Math.random();
      this.a = rand(0, 360);
      this.rad = this.a * Math.PI / 180;
      this.as = rand(0, 360) * Math.PI / 180;
    };
    Bubble.prototype.draw = function() {
      let ctx  = this.ctx;
      ctx.save();
      ctx.fillStyle = 'white';
      ctx.strokeStyle = 'white';
      ctx.lineCap = 'round';
      ctx.lineWidth = this.r / 4;
      ctx.globalAlpha = this.ga;
      ctx.translate(this.x, this.y);
      ctx.rotate(this.rad);
      ctx.translate(-this.x, -this.y);
      ctx.beginPath();
      ctx.arc(this.x, this.y, this.r, 0, Math.PI * 2, false);
      ctx.fill();
      ctx.globalAlpha = this.ga * 1.1;
      ctx.beginPath();
      ctx.arc(this.x, this.y, this.r * 0.7, this.as, this.as + 1, false);
      ctx.stroke();
      ctx.restore();
    };
    Bubble.prototype.updatePosition = function() {
      if (this.y > Y - Y / 3) {
        this.v.x += 0.1;
        this.v.y -= 0.01;
      }
      this.x += this.v.x;
      this.y += this.v.y;
    };
    Bubble.prototype.updateParams = function(i) {
      this.a += this.random;
      this.rad = this.a * Math.PI / 180;
    };
    Bubble.prototype.wrapPosition = function() {
      if (this.x > X + this.r / 2) {
        this.init(rand(0, X), rand(0 - Y / 5, 0));
      }
    };
    Bubble.prototype.render = function(i) {
      this.updateParams(i);
      this.updatePosition();
      this.wrapPosition();
      this.draw();
    };
    for (let i = 0; i < bubbleNum; i++) {
      let b = new Bubble(ctx, rand(0, X), rand(0, Y / 2));
      bubbles.push(b);
    }
    function Shape(ctx, x, y) {
      this.ctx = ctx;
      this.init(x, y);
    }
    Shape.prototype.init = function(x, y) {
      this.x = x;
      this.y = y;
      this.r = rand(20, 30);
      this.a = 0;
      this.rad = this.a * Math.PI / 180;
      this.random = Math.random();
      this.c = rand(0, 360);
      this.a1 = rand(-10, 10);
      this.rad1 = this.a1 * Math.PI / 180;
    };
    Shape.prototype.draw = function() {
      let ctx  = this.ctx;
      ctx.save();
      ctx.fillStyle = 'hsl(' + this.c + ', 100%, 80%)';
      ctx.strokeStyle = 'hsl(' + this.c + ', 80%, 60%)';
      ctx.translate(this.x, this.y);
      ctx.rotate(this.rad1);
      ctx.translate(-this.x, -this.y);
      ctx.lineWidth = this.r / 10;
      ctx.beginPath();
      ctx.moveTo(this.x, this.y);
      ctx.lineTo(this.x, Y + 10);
      ctx.stroke();
      ctx.lineWidth = 1;
      ctx.translate(this.x, this.y);
      ctx.rotate(Math.tan(this.rad));
      ctx.translate(-this.x, -this.y);
      ctx.fillRect(this.x - this.r, this.y - this.r, this.r * 2, this.r * 2);
      ctx.fillStyle = 'hsl(' + this.c + ', 80%, 60%)';
      for (let j = 0; j < 4; j++) {
        ctx.translate(this.x, this.y);
        ctx.rotate(90 * Math.PI / 180);
        ctx.translate(-this.x, -this.y);
        ctx.beginPath();
        ctx.moveTo(Math.cos(rad * 0) * this.r + this.x, Math.sin(rad * 0) * this.r + this.y + this.r);
        for (let i = 1; i < 4; i++) {
          if (i !== 2) {
            ctx.lineTo(Math.cos(rad * i) * this.r + this.x, Math.sin(rad * i) * this.r + this.y + this.r);
          }
        }
        ctx.closePath();
        ctx.fill();
      }
      ctx.restore();
    };
    Shape.prototype.updateParams = function() {
      this.a += this.random;
      this.rad = this.a * Math.PI / 180;
    };
    Shape.prototype.render = function(i) {
      this.updateParams();
      this.draw();
    };
    for (let i = 0; i < X;) {
      let dist = rand(1, 50);
      let s = new Shape(ctx, i += dist, rand(Y - Y / 3, Y - Y / 6));
      shapes.push(s);
    }
    function render() {
      ctx.clearRect(0, 0, X, Y);
      for (let i = 0; i < shapes.length; i++) {
        shapes[i].render(i);
      }
      for (let i = 0; i < bubbles.length; i++) {
        bubbles[i].render(i);
      }
      requestAnimationFrame(render);
    }
    render();
    function onResize() {
      X = canvas.width = window.innerWidth;
      Y = canvas.height = window.innerHeight;
      if (X < 768) {
        bubbleNum = 100;
      } else {
        bubbleNum = 200;
      }
      shapes = [];
      bubbles = [];
      for (let i = 0; i < X;) {
        let dist = rand(1, 50);
        let s = new Shape(ctx, i += dist, rand(Y - Y / 3, Y - Y / 6));
        shapes.push(s);
      }
      for (let i = 0; i < bubbleNum; i++) {
        let b = new Bubble(ctx, rand(0, X), rand(0, Y / 2));
        bubbles.push(b);
      }
    }
    window.addEventListener('resize', function() {
      onResize();
    });
    canvas.addEventListener('click', function(e) {
      mouseX = e.clientX;
      mouseY = e.clientY;
      let num = rand(1, 20);
      for (let i = 0; i < num; i++) {
        let b = new Bubble(ctx, rand(mouseX - 100, mouseX + 100), rand(mouseY - 100, mouseY + 100));
        bubbles.push(b);
      }
    }, false)
    }
  }
}
</script>
<style lang="css">
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap");

* {
box-sizing: border-box;
padding: 0;
margin: 0;
}
canvas#canvas {
display: block;
background: #ABE7FF;
}
.main-container {
background: #ecfffc;
/* color: #7e9dff; */
width: 500px;
margin: auto;
border-radius: 10px;
position: absolute;
top: 40px;
right: 40px;
}

h4 {
color: #7e9dff;
opacity: 0.7;
}

ul {
list-style: none;
}

a {
text-decoration: none;
}

.calendar-head {
display: flex;
justify-content: space-between;
padding: 30px;
border-bottom: 2px solid #7e9dff;
}

.calendar-body {
padding: 30px;
text-align: center;
}

.weekdays {
text-transform: uppercase;
color: #7e9dff;
font-weight: bold;
font-size: 0.9rem;
display: grid;
grid-template-columns: repeat(7, 1fr);
margin-bottom: 10px;
}

.days {
display: grid;
grid-template-columns: repeat(7, 1fr);
}

.days li {
padding: 10px 0;
cursor: pointer;
position: relative;
}

.days li:hover {
color: #c74b43;
}

.previous-month {
opacity: 0.2;
}

.date-with-event {
border: 2px solid #7e9dff;
padding: 10px;
border-radius: 50%;
}

.date-with-event:hover {
background: #7e9dff;
color: #ecfffc;
font-weight: bold;
}

.event-count {
position: absolute;
top: 0;
right: 5px;
font-size: 0.6rem;
background: #c74b43;
color: #fff;
display: block;
padding: 2px 5px;
border-radius: 50px;
}

.active {
/* background: #7e9dff; */
color: #db3341 !important;
font-weight: bold;
/* padding: 10px;
border-radius: 50%; */
width: 100px;
height: 90px;
position: relative;
}
.active_text{
color: #db3341 !important;
position: relative;
}
.active:before,
.active:after {
width: 20px;
height: 29px;
left: 8px;
top: -3px;
background-color: #e28ad6;
position: absolute;
content: "";
border-radius: 50px 50px 0 0;
transform: rotate(-45deg);
transform-origin: 0 100%;
}
.active:after {
left: -11px;
transform: rotate(45deg);
transform-origin: 100% 100%;
}
.active2:before,
.active2:after {
width: 20px;
height: 29px;
left: 4px;
top: -3px;
background-color: #e28ad6;
position: absolute;
content: "";
border-radius: 50px 50px 0 0;
transform: rotate(-45deg);
transform-origin: 0 100%;
}
.active2:after {
left: -15px;
transform: rotate(45deg);
transform-origin: 100% 100%;
}

.calendar-footer {
display: flex;
align-items: center;
justify-content: space-between;
padding: 30px;
border-top: 2px solid #7e9dff;
}

.add-event-btn {
color: #7e9dff;
padding: 10px 15px;
border: 2px solid #7e9dff;
border-radius: 50%;
}

.add-event-btn:hover {
background: #7e9dff;
color: #ecfffc;
}
.A img:nth-child(1) {
height: 300px;
width: 500px;
transition: ease-in 4s;
position: absolute;
top: 50px;
left: 40px;
transform: rotate(-12deg);
}
.A img:nth-child(2) {
/* height: 300px; */
width: 215px;
transition: ease-in 4s;
position: absolute;
top: 50px;
left: 600px;
transform: rotate(15deg);
}
.B img:nth-child(1) {
height: 200px;
position: absolute;
top: 50px;
left: 40px;
transform: rotate(-12deg);
}
.B img:nth-child(2) {
width: 300px;
position: absolute;
top: 50px;
left: 600px;
transform: rotate(15deg);
}
.B img:nth-child(3) {
width: 600px;
position: absolute;
top: 260px;
left: 400px;
}
</style>
