<template>
<div v-if="bol" class="wrap">
  <div class="toubu"></div>
  <div class="zjt">
    <img src="/static/img/zuo.png" alt="" @click="fh()">
  </div>
  <p class="p1">健康美味兼得的布尔本</p>
  <div class="fx">
    <img src="/static/img/fengxiang.png" alt="">
  </div>
  <div class="diyiye">
    <img src="/static/img/datu.png" alt="">
  </div>
  <div class="jj">
    <div class="wb">
      日本著名糕点品牌Bourbon布尔本，成立于1924年,
    </div>
    <div class="wb1">
      是日本零食十强之一。制作的曲奇和糕点系列,品质
    </div>
    <div class="wb2">
      远胜于欧洲传统西点,做工研究、精致、高贵、时尚、
    </div>
    <div class="wb3">
      健康是Bourbon一贯的严谨作风,其北日本系列礼盒
    </div>
    <div class="wb4">
      更是夺得了销售冠军,相当受欢迎。
    </div>
  </div>
  <div class="zj">
    <div class="bg">
      <img src="/static/img/binggan001.png" alt="">
    </div>
    <div class="wel">
      最受欢迎曲奇礼盒系列
    </div>
    <div class="jp">
      <p>
        日本本土国内受欢迎的曲奇点心，浓浓 <br>
        的牛油味，饼干的酥脆和可可牛奶的美 <br>
        妙结合，咬下去，满满幸福感。礼盒装 <br>
        有三种不同口味，一盒里约54枚，布尔 <br>
        本家产品，礼盒包装无论是送人还是留 <br>
      </p>
    </div>
    <div class="xw">
      着自己下午茶，都非常合适。
    </div>
  </div>
  <div class="hkl">
  <div class="kitty">
    <img :src="arr[17].src" alt="">
  </div>
    <div class="x"></div>
    <div class="bb">
      BOURBON布尔本hello kitty
    </div>
    <div class="quqi">
      黄油曲奇礼盒54枚
    </div>
    <div class="pirce">
      {{arr[17].jiage}}
    </div>
    <div class="m">
      <img src="/static/img/changyuan.png" alt="">
    </div>
    <div class="mai">
      马上购买
    </div>
    <div class="hkl1">
      <div class="kitty1">
        <img :src="arr[17].src" alt="">
      </div>
      <div class="x1"></div>
      <div class="bb1">
        BOURBON布尔本hello kitty
      </div>
      <div class="quqi1">
        黄油曲奇礼盒54枚
      </div>
      <div class="pirce1">
        {{arr[17].jiage}}
      </div>
      <div class="m1">
        <img src="/static/img/changyuan.png" alt="">
      </div>
      <div class="mai1">
        马上购买
      </div>
  </div>
    <div class="hkl2">
      <div class="kitty2">
        <img :src="arr[17].src" alt="">
      </div>
      <div class="x2"></div>
      <div class="bb2">
        BOURBON布尔本hello kitty
      </div>
      <div class="quqi2">
        黄油曲奇礼盒54枚
      </div>
      <div class="pirce2">
        {{arr[17].jiage}}
      </div>
      <div class="m2">
        <img src="/static/img/changyuan.png" alt="">
      </div>
      <div class="mai2">
        马上购买
      </div>
 </div>
    <div class="hkl3">
      <div class="kitty3">
        <img :src="arr[17].src" alt="">
      </div>
      <div class="x3"></div>
      <div class="bb3">
        BOURBON布尔本hello kitty
      </div>
      <div class="quqi3">
        黄油曲奇礼盒54枚
      </div>
      <div class="pirce3">
        {{arr[17].jiage}}
      </div>
      <div class="m3">
        <img src="/static/img/changyuan.png" alt="">
      </div>
      <div class="mai3">
        马上购买
      </div>
 </div>
  </div>
  <div class="zj1">
    <div class="bg1">
      <img src="/static/img/binggan001.png" alt="">
    </div>
    <div class="wel1">
      最受欢迎曲奇礼盒系列
    </div>
    <div class="jp1">
      <p>
        日本本土国内受欢迎的曲奇点心，浓浓 <br>
        的牛油味，饼干的酥脆和可可牛奶的美 <br>
        妙结合，咬下去，满满幸福感。礼盒装 <br>
        有三种不同口味，一盒里约54枚，布尔 <br>
        本家产品，礼盒包装无论是送人还是留 <br>
      </p>
    </div>
    <div class="xw1">
      着自己下午茶，都非常合适。
    </div>
  </div>
  <div class="hkl4">
    <div class="kitty4">
      <img :src="arr[17].src" alt="">
    </div>
    <div class="x4"></div>
    <div class="bb4">
      BOURBON布尔本hello kitty
    </div>
    <div class="quqi4">
      黄油曲奇礼盒54枚
    </div>
    <div class="pirce4">
      {{arr[17].jiage}}
    </div>
    <div class="m4">
      <img src="/static/img/changyuan.png" alt="">
    </div>
    <div class="mai4">
      马上购买
    </div>
    <div class="hkl5">
      <div class="kitty5">
        <img :src="arr[17].src" alt="">
      </div>
      <div class="x5"></div>
      <div class="bb5">
        BOURBON布尔本hello kitty
      </div>
      <div class="quqi5">
        黄油曲奇礼盒54枚
      </div>
      <div class="pirce5">
        {{arr[17].jiage}}
      </div>
      <div class="m5">
        <img src="/static/img/changyuan.png" alt="">
      </div>
      <div class="mai5">
        马上购买
      </div>
    </div>
    <div class="hkl6">
      <div class="kitty6">
        <img :src="arr[17].src" alt="">
      </div>
      <div class="x6"></div>
      <div class="bb6">
        BOURBON布尔本hello kitty
      </div>
      <div class="quqi6">
        黄油曲奇礼盒54枚
      </div>
      <div class="pirce6">
        {{arr[17].jiage}}
      </div>
      <div class="m6">
        <img src="/static/img/changyuan.png" alt="">
      </div>
      <div class="mai6">
        马上购买
      </div>
    </div>
    <div class="hkl7">
      <div class="kitty7">
        <img :src="arr[17].src" alt="">
      </div>
      <div class="x7"></div>
      <div class="bb7">
        BOURBON布尔本hello kitty
      </div>
      <div class="quqi7">
        黄油曲奇礼盒54枚
      </div>
      <div class="pirce7">
        {{arr[17].jiage}}
      </div>
      <div class="m7">
        <img src="/static/img/changyuan.png" alt="">
      </div>
      <div class="mai7">
        马上购买
      </div>
    </div>
  </div>
  </div>
</template>
<script>
    import axios from 'axios'
    export default {
        name: "Shang",
        data(){
          return{
            bol:false,
            arr:[]
          }
        },
        methods:{
          fh(){
            this.$router.push('/shouye')
          }
        },
        mounted: function () {
          axios.get('/api/phph0302/zh01.php').then((res)=>{
            this.bol=true;
            this.arr=res.data
          })
        }
    }
</script>

<style scoped>
.wrap{
  margin: 0;
  padding: 0;
  width: 100%;
  position: relative;
}
.toubu{
  position: absolute;
  border: 1px solid rgb(229,62,66);
  width: 72rem;
  height: 9.6rem;
  background-color: rgb(229,62,66);
}
.zjt img{
  position: absolute;
  left:3rem;
  top: 4rem;
  width: 2.3rem;
  height: 3.8rem;
}
.p1{
  position: absolute;
  font-size: 3.6rem;
  color: white;
  left: 17rem;
  top: 3.5rem;
}
.fx img{
  position: absolute;
  width: 3.6rem;
  height: 3.4rem;
  top: 4.5rem;
  left: 63rem;
}
  .diyiye img{
    position: absolute;
    width:72rem;
    height: 40rem;
    top: 9.5rem;
    left: 0.01rem;
  }
  .jj{
    position: absolute;
    background-color:rgb(255,205,44);
    border: 1px solid rgb(255,205,44);
    top: 49.5rem;
    width:72rem;
    height: 24rem;
  }
  .wb{
    position: absolute;
   font-size: 2.8rem;
    top: 3rem;
    left: 3rem;
  }
  .wb1{
    position: absolute;
    font-size: 2.8rem;
    top: 6rem;
    left: 3rem;
  }
  .wb2{
    position: absolute;
    font-size: 2.8rem;
    top: 9rem;
    left: 3rem;
  }
   .wb3{
     position: absolute;
     font-size: 2.8rem;
     top: 12rem;
     left: 3rem;
   }
  .wb4{
    position: absolute;
    font-size: 2.8rem;
    top: 15rem;
    left: 3rem;
  }
  .zj{
    position: relative;
    /*border: 1px solid wheat;*/
    background-color: whitesmoke;
    top: 77rem;
    width: 68rem;
    height: 40rem;
    left: 2rem;
  }
  .bg img{
    position: absolute;
    width: 22rem;
    height: 36rem;
    top: 2rem;
    left: 2rem;
  }
  .wel{
    position: absolute;
    font-size: 3rem;
    font-family: MicrosoftYaHei;
    color:rgb(78,31,29);
    left: 25rem;
    top: 3.5rem;
  }
  .jp p{
    position: absolute;
    font-size: 2.4rem;
    font-family: MicrosoftYaHei;
    color: rgb(77,77,77);
    left: 24.5rem;
    top: 9rem;
  }
  .xw{
    position: absolute;
    font-size: 2.4rem;
    font-family: MicrosoftYaHei;
    color: rgb(77,77,77);
    left: 24.5rem;
    top: 26rem;
  }
  .hkl{
    position: relative;
    background-color: whitesmoke;
    /*border: 1px solid deeppink;*/
    top: 80rem;
    width: 33rem;
    height: 44rem;
    left: 2rem;
  }
  .kitty img{
    position: absolute;
    width: 17.2rem;
    height: 17.2rem;
    top: 5rem;
    left: 8rem;
  }
  .x{
    position: absolute;
    border: 1px solid gainsboro;
    width: 33rem;
    height: 0.1rem;
    top: 26rem;
  }
  .bb{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(77,77,77);
    font-family: SimHei;
    top: 28rem;
    left: 1rem;
  }
  .quqi{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(77,77,77);
    font-family: SimHei;
    top: 31.5rem;
    left: 1rem;
  }
  .pirce{
    position: absolute;
    font-size: 2.4rem;
    color: rgb(229,62,66);
    font-family: MicrosoftYaHei;
    top: 35rem;
    left: 12rem;
  }
  .m img{
    position: absolute;
    width: 21.8rem;
    height: 3rem;
    top: 39rem;
    left: 5rem;
  }
  .mai{
    position: absolute;
    font-size: 1.8rem;
    color: rgb(255,255,255);
    top: 39.2rem;
    left: 12rem;
  }
.hkl1{
  position: relative;
  background-color: whitesmoke;
  /*border: 1px solid deeppink;*/
  top: 0.2rem;
  width: 33rem;
  height: 44rem;
  left:35rem;
}
.kitty1 img{
  position: absolute;
  width: 17.2rem;
  height: 17.2rem;
  top: 5rem;
  left: 8rem;
}
.x1{
  position: absolute;
  border: 1px solid gainsboro;
  width: 33rem;
  height: 0.1rem;
  top: 26rem;
}
.bb1{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 28rem;
  left: 1rem;
}
.quqi1{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 31.5rem;
  left: 1rem;
}
.pirce1{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(229,62,66);
  font-family: MicrosoftYaHei;
  top: 35rem;
  left: 12rem;
}
.m1 img{
  position: absolute;
  width: 21.8rem;
  height: 3rem;
  top: 39rem;
  left: 5rem;
}
.mai1{
  position: absolute;
  font-size: 1.8rem;
  color: rgb(255,255,255);
  top: 39.2rem;
  left: 12rem;
}
.hkl2{
  position: relative;
  background-color: whitesmoke;
  /*border: 1px solid deeppink;*/
  top: 1.5rem;
  width: 33rem;
  height: 44rem;
  left:35rem;
}
.kitty2 img{
  position: absolute;
  width: 17.2rem;
  height: 17.2rem;
  top: 5rem;
  left: 8rem;
}
.x2{
  position: absolute;
  border: 1px solid gainsboro;
  width: 33rem;
  height: 0.1rem;
  top: 26rem;
}
.bb2{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 28rem;
  left: 1rem;
}
.quqi2{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 31.5rem;
  left: 1rem;
}
.pirce2{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(229,62,66);
  font-family: MicrosoftYaHei;
  top: 35rem;
  left: 12rem;
}
.m2 img{
  position: absolute;
  width: 21.8rem;
  height: 3rem;
  top: 39rem;
  left: 5rem;
}
.mai2{
  position: absolute;
  font-size: 1.8rem;
  color: rgb(255,255,255);
  top: 39.2rem;
  left: 12rem;
}
.hkl3{
  position: relative;
  background-color: whitesmoke;
  /*border: 1px solid deeppink;*/
  top: -42rem;
  width: 33rem;
  height: 44rem;
  left:0.3rem;
}
.kitty3 img{
  position: absolute;
  width: 17.2rem;
  height: 17.2rem;
  top: 5rem;
  left: 8rem;
}
.x3{
  position: absolute;
  border: 1px solid gainsboro;
  width: 33rem;
  height: 0.1rem;
  top: 26rem;
}
.bb3{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 28rem;
  left: 1rem;
}
.quqi3{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 31.5rem;
  left: 1rem;
}
.pirce3{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(229,62,66);
  font-family: MicrosoftYaHei;
  top: 35rem;
  left: 12rem;
}
.m3 img{
  position: absolute;
  width: 21.8rem;
  height: 3rem;
  top: 39rem;
  left: 5rem;
}
.mai3{
  position: absolute;
  font-size: 1.8rem;
  color: rgb(255,255,255);
  top: 39.2rem;
  left: 12rem;
}
.zj1{
  position: relative;
  /*border: 1px solid wheat;*/
  background-color: whitesmoke;
  top: 129rem;
  width: 68rem;
  height: 40rem;
  left: 2rem;
}
.bg1 img{
  position: absolute;
  width: 22rem;
  height: 36rem;
  top: 2rem;
  left: 2rem;
}
.wel1{
  position: absolute;
  font-size: 3rem;
  font-family: MicrosoftYaHei;
  color:rgb(78,31,29);
  left: 25rem;
  top: 3.5rem;
}
.jp1 p{
  position: absolute;
  font-size: 2.4rem;
  font-family: MicrosoftYaHei;
  color: rgb(77,77,77);
  left: 24.5rem;
  top: 9rem;
}
.xw1{
  position: absolute;
  font-size: 2.4rem;
  font-family: MicrosoftYaHei;
  color: rgb(77,77,77);
  left: 24.5rem;
  top: 26rem;
}
.hkl4{
  position: relative;
  background-color: whitesmoke;
  /*border: 1px solid deeppink;*/
  top: 132rem;
  width: 33rem;
  height: 44rem;
  left: 2rem;
}
.kitty4 img{
  position: absolute;
  width: 17.2rem;
  height: 17.2rem;
  top: 5rem;
  left: 8rem;
}
.x4{
  position: absolute;
  border: 1px solid gainsboro;
  width: 33rem;
  height: 0.1rem;
  top: 26rem;
}
.bb4{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 28rem;
  left: 1rem;
}
.quqi4{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 31.5rem;
  left: 1rem;
}
.pirce4{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(229,62,66);
  font-family: MicrosoftYaHei;
  top: 35rem;
  left: 12rem;
}
.m4 img{
  position: absolute;
  width: 21.8rem;
  height: 3rem;
  top: 39rem;
  left: 5rem;
}
.mai4{
  position: absolute;
  font-size: 1.8rem;
  color: rgb(255,255,255);
  top: 39.2rem;
  left: 12rem;
}
.hkl5{
  position: relative;
  background-color: whitesmoke;
  /*border: 1px solid deeppink;*/
  top: 0.2rem;
  width: 33rem;
  height: 44rem;
  left:35rem;
}
.kitty5 img{
  position: absolute;
  width: 17.2rem;
  height: 17.2rem;
  top: 5rem;
  left: 8rem;
}
.x5{
  position: absolute;
  border: 1px solid gainsboro;
  width: 33rem;
  height: 0.1rem;
  top: 26rem;
}
.bb5{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 28rem;
  left: 1rem;
}
.quqi5{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 31.5rem;
  left: 1rem;
}
.pirce5{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(229,62,66);
  font-family: MicrosoftYaHei;
  top: 35rem;
  left: 12rem;
}
.m5 img{
  position: absolute;
  width: 21.8rem;
  height: 3rem;
  top: 39rem;
  left: 5rem;
}
.mai5{
  position: absolute;
  font-size: 1.8rem;
  color: rgb(255,255,255);
  top: 39.2rem;
  left: 12rem;
}
.hkl6{
  position: relative;
  background-color: whitesmoke;
  /*border: 1px solid deeppink;*/
  top: 1.5rem;
  width: 33rem;
  height: 44rem;
  left:35rem;
}
.kitty6 img{
  position: absolute;
  width: 17.2rem;
  height: 17.2rem;
  top: 5rem;
  left: 8rem;
}
.x6{
  position: absolute;
  border: 1px solid gainsboro;
  width: 33rem;
  height: 0.1rem;
  top: 26rem;
}
.bb6{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 28rem;
  left: 1rem;
}
.quqi6{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 31.5rem;
  left: 1rem;
}
.pirce6{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(229,62,66);
  font-family: MicrosoftYaHei;
  top: 35rem;
  left: 12rem;
}
.m6 img{
  position: absolute;
  width: 21.8rem;
  height: 3rem;
  top: 39rem;
  left: 5rem;
}
.mai6{
  position: absolute;
  font-size: 1.8rem;
  color: rgb(255,255,255);
  top: 39.2rem;
  left: 12rem;
}
.hkl7{
  position: relative;
  background-color: whitesmoke;
  /*border: 1px solid deeppink;*/
  top: -42.5rem;
  width: 33rem;
  height: 44rem;
  left:0.3rem;
}
.kitty7 img{
  position: absolute;
  width: 17.2rem;
  height: 17.2rem;
  top: 5rem;
  left: 8rem;
}
.x7{
  position: absolute;
  border: 1px solid gainsboro;
  width: 33rem;
  height: 0.1rem;
  top: 26rem;
}
.bb7{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 28rem;
  left: 1rem;
}
.quqi7{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(77,77,77);
  font-family: SimHei;
  top: 31.5rem;
  left: 1rem;
}
.pirce7{
  position: absolute;
  font-size: 2.4rem;
  color: rgb(229,62,66);
  font-family: MicrosoftYaHei;
  top: 35rem;
  left: 12rem;
}
.m7 img{
  position: absolute;
  width: 21.8rem;
  height: 3rem;
  top: 39rem;
  left: 5rem;
}
.mai7{
  position: absolute;
  font-size: 1.8rem;
  color: rgb(255,255,255);
  top: 39.2rem;
  left: 12rem;
}
</style>


