<template>
  <div class="wrap">
    <div class="top">
      <img @click="ba()" src="/static/img/fanhui.png" alt="">
      <span>阿拉粉心得</span>
    </div>
    <div class="two">
      <span :class="[hui,{hong:bol1}]" @click="xinde()">全部心得</span>
      <span :class="[hui,{hong:bol2}]" @click="shaitu()">晒图</span>
      <div v-show="bol1" class="xian"></div>
      <div v-show="bol2" class="xian2"></div>
    </div>

    <div v-show="bol1">
      <div class="xinde02">
      <div class="nicheng"><router-link to="/xindede"><img src="/static/img/xinderen.png" alt=""></router-link></div>
      <span style="left:12rem;top: 2.2rem;">昵称</span>
      <span style="right: 1rem;top: 2.2rem;color: #808080;">2018-7-14</span>
      <p>法司法和后三个我获得父回归到符合股份官方价格法规回复黄金国际化高合金钢感觉好贵.............................</p>

      <div class="huifu">
       <div> <img src="/static/img/dianzan.png" alt=""> <span> 1</span> </div><div class="xieg"></div>
        <div><img src="/static/img/pinglun.png" alt=""> <span> 10</span> </div><div class="xieg02"> </div>
       <div> <img src="/static/img/xiaofen.png" alt=""> <span> 26</span></div>
      </div>
      </div>
      <div class="xinde02">
        <div style="margin-top: 2rem;" class="nicheng"><router-link to="/xindede"><img src="/static/img/xinderen.png" alt=""></router-link></div>
        <span style="left:12rem;top: 2.2rem;">昵称</span>
        <span style="right: 1rem;top: 2.2rem;color: #808080;">2018-7-14</span>
        <p>法司法和后三个我获得父回归到符合股份官方价格法规回复黄金国际化高合金钢感觉好贵.............................</p>
        <br><br>
        <div class="chuantu">
       <button>添加图片</button>
        </div>
        <div class="huifu">
          <div> <img src="/static/img/dianzan.png" alt=""> <span> 1</span> </div><div class="xieg"></div>
          <div><img src="/static/img/pinglun.png" alt=""> <span> 10</span> </div><div class="xieg02"> </div>
          <div> <img src="/static/img/xiaofen.png" alt=""> <span> 26</span></div>
        </div>
        <div class="dibu">
          <span>加载更多</span>
        </div>
      </div>

    </div>

    <div v-show="bol2" class="shaitu02">
      <div class="xinde02">
        <div class="nicheng"><router-link to="/xindede"><img src="/static/img/xinderen.png" alt=""></router-link></div>
        <span style="left:12rem;top: 2.2rem;">昵称</span>
        <span style="right: 1rem;top: 2.2rem;color: #808080;">2018-7-14</span>
        <p>法司法和后三个我获得父回归到符合股份官方价格法规回复黄金国际化高合金钢感觉好贵.............................</p>
        <br><br>
        <div class="chuantu">
          <button>添加图片</button>
        </div>
        <div class="huifu">
          <div> <img src="/static/img/dianzan.png" alt=""> <span> 1</span> </div><div class="xieg"></div>
          <div><img src="/static/img/pinglun.png" alt=""> <span> 10</span> </div><div class="xieg02"> </div>
          <div> <img src="/static/img/xiaofen.png" alt=""> <span> 26</span></div>
        </div>
        <div class="dibu">
          <span>加载更多</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Xinde",
        data(){
          return {
            bol1:true,
            bol2:false,
            hui:'hui',
            hong:'hong'
          }
        },
      methods:{
        xinde(){
          this.bol2 = false;
        this.bol1 =true;

        },
        shaitu(){
          this.bol2 = true;
          this.bol1 =false;
        },
        ba(){
          this.$router.push("/xiangqing")
        }

      }
    }
</script>

<style scoped>
  *{margin: 0;padding: 0;}
  .wrap{width: 100%;background-color: #f2f2f2;}
  .top{background-color: red;
    height: 9.6rem;
    width: 100%;
    text-align: center;
    line-height: 9.6rem;
  }
  .top img:nth-child(1){
    width: 2.3rem;
    height: 3.8rem;
    float: left;
    margin-left: 2rem;
    margin-top: 3rem;
  }
  .top span{font-size: 3.6rem;color: white;
  display: inline-block;
  }
  .two{
    width: 100%;
    height: 9.6rem;
    line-height: 9.6rem;
    text-align: center;
    border-bottom: 1px dimgray solid;
    position: relative;
    background-color: white;
  }
  .two span{
    display: inline-block;
    width: 49.7%;
    font-size: 3rem;

  }
  .two span:nth-child(1){
    background-color: white;
    border-right: 1px dimgray solid;
  }

.xian{
  width: 12.1rem;
  height: 3px;
  background-color: red;
  position: absolute;
  bottom: 0;
  left: 11.9rem;

}
  .xian2{
    width: 12.1rem;
    height: 3px;
    background-color: red;
    position: absolute;
    bottom: 0;
    right: 11.9rem;
  }
  .hui{
    color: grey;
  }
  .hong{
    color: red;
  }
  .nicheng{
    width: 8rem;
    height: 8rem;
    border: 1px #cccccc solid;
    border-radius: 50%;
    margin-left: 2rem;

    text-align: center;
    line-height:12rem;

  }
  .nicheng img{
    width: 8rem;
    height: 8rem;
  }
  .xinde02{position: relative;
    width: 100%;
    height: 32rem;
    background-color: white;
  }
.xinde02 span{font-size: 2.8rem;position: absolute;}
.xinde02 p{
  font-size: 2.4rem;
  width: 66.6rem;
  height: 5.9rem;
  margin-left: 3.3rem;
  margin-top: 2rem;
  color: #808080;
}
.huifu{
  width: 100%;
  position: relative;
  border-top: 1px #cccccc solid;
  line-height: 3rem;
  display: flex;
  margin-top: 3rem;
  justify-content: space-around;
  background-color: white;
}
.huifu div{
  margin-top: 4.8rem;
  width: 5rem;
  line-height: 2rem;
}
  .huifu div span{
    display: inline-block;
    margin-top: -2.6rem;
    padding: 3rem;
    color: #cccccc;
  }
.huifu div img{
  width: 2.4rem;
  height: 2.4rem;
}
.xieg,.xieg02{
  position: absolute;
  border-left: 1px #cccccc solid;
  width: 1rem;
  height: 6rem;
}
.xieg{
  left: 25rem;
  top:-2rem;
}
  .xieg02{
    right: 17rem;
    top:-2rem;

  }

 .chuantu{
   width: 26rem;
   height: 20rem;
   border: 1px #cccccc solid;
   margin-left: 5rem;
   line-height: 20rem;
   text-align: center;
 }
.chuantu button{
  font-size: 3rem;
  width: 20rem;
  height: 8rem;
  color: black;
  text-align: center;
  border-radius: 2rem;
  background: #0f0;
}

  .dibu{
    background-color: #f2f2f2;
    width: 100%;
    margin-top: 2rem;
    text-align: center;
    line-height: 14.4rem;
  }
  .dibu span {
    margin-left: -4rem;
    color: #cccccc;
  }
</style>
