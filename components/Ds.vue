<template>
  <p>倒计时:{{hour}}:{{minute}}:{{second}}</p>
</template>

<script>
    export default {
        name: "Ds",
      data () {
        return {
          hours:3,
          minutes: 2,
          seconds: 56
        }
      },
      mounted () {
        this.add()
      },
      methods: {

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
  p{
    font-size: 3rem;
    color: #f00;
  }
</style>
