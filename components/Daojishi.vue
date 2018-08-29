<template>
  <div class="bottom">
    <p>共计1件商品 合计 : ¥166.06(含运费 : ¥1.00)</p>
    <button>催单</button>
    <button class="btn1" @click="qx()">取消订单</button>
    <p class="pq1">{{hour}}:{{minute}}:{{second}}</p>
  </div>

</template>

<script>
    export default {
        name: "Daojishi",
      data () {
        return {
          hours:5,
          minutes: 0,
          seconds: 0
        }
      },
      mounted () {
        this.add()
      },
      methods: {
        qx(){
          $(".bo").remove();
        },
        num: function (n) {
          return n < 10 ? '0' + n : '' + n
        },
        add: function () {
          var _this = this;
          var time = window.setInterval(function () {
            if (_this.seconds == 0 && _this.minutes != 0 && _this.hours != 0) {
              _this.seconds = 59
              _this.minutes -= 1
            } else if (_this.minutes == 0 && _this.seconds == 0 && _this.hours == 0) {
              _this.seconds = 0
              window.clearInterval(time)
              document.getElementsByClassName("btn1")[0].style.background="#ccc";
              document.getElementsByClassName("pq1")[0].innerHTML="";
            } else if (_this.minutes == 0 && _this.seconds == 0 && _this.hours != 0) {
              _this.seconds = 59;
              _this.minutes = 59;
              _this.hours -= 1;
            }else{
              _this.seconds -= 1
            }
          }, 1000);
        }
      },
      watch: {
        second: {
          handler (newVal) {
            this.num(newVal)
          }
        },
        minute: {
          handler (newVal) {
            this.num(newVal)
          }
        },
        hour: {
          handler (newVal) {
            this.num(newVal)
          }
        }
      },
      computed: {
        second: function () {
          return this.num(this.seconds)
        },
        minute: function () {
          return this.num(this.minutes)
        },
        hour: function () {
          return this.num(this.hours)
        }
      }
    }
</script>

<style scoped>
  .pq1{
    position: absolute;
    right: 3.5rem;
    bottom: -1rem;
    font-size: 1.8rem;
    color: #f00;
  }
  .bottom{
    width: 100%;
    height: 12.2rem;
    background-color: #fff;
    position: relative;
  }
  .bottom p{
    float: right;
    margin-right: 2rem;
    margin-top: 2rem;
    font-size: 2.4rem;
  }
  .bottom button{
    width: 12.7rem;
    height: 4rem;
    background-color: #f00;
    color: #fff;
    border-radius: 2rem;
    font-size: 2.4rem;
  }
  .bottom button:nth-child(2){
    position: absolute;
    right: 20rem;
    bottom: 2rem;
  }
  .bottom button:nth-child(3){
    position: absolute;
    right: 4rem;
    bottom: 2rem;
  }
</style>
