<template>
    <div class="wrap">
      <div class="top" @click="s()">
        <img @click="ba()" src="/static/img/fanhui.png" alt="" class="inp">
        <div>
          <input type="text" value="" placeholder="输入商品关键字">
          <img src="/static/img/sousuo.png" alt="" class="sousuo">
        </div>
        <span class="fx" @click="ss()">搜索</span>
      </div>
      <div class="bb">
        <p>亲们都在找</p>
      </div>
      <div class="bc">
        <button @click="ss()">面膜</button>
        <button @click="ss()">防晒</button>
        <button @click="ss()">眼霜</button>
        <button @click="ss()">精华</button>
      </div>
      <div class="bc">
        <button @click="ss()">洗面奶</button>
        <button @click="ss()">资生堂</button>
        <button @click="ss()">洗发水</button>
        <button @click="ss()">防晒喷雾</button>
      </div>
      <div class="bc">
        <button @click="ss()">洗面奶</button>
        <button @click="ss()">资生堂</button>
        <button @click="ss()">洗发水</button>
        <button @click="ss()">防晒喷雾</button>
      </div>
      <div class="suo" v-show="bol1">
        <p @click="zz()">最近搜索</p>
        <ul class="ul1">
          <li v-for="item in arr">{{item}}</li>
          <li v-show="bol">{{item}}</li>
        </ul>
        <button @click="chuchu()">清空搜索历史</button>
      </div>
    </div>
</template>

<script>
    export default {
        name: "Sousuo",
        data(){
          return{
            val:'',
            arr:[],
            item:"筱倩",
            bol:false,
            bol1:false
          }
        },
        methods:{
          ba(){
            this.$router.push("/shouye");
          },
          ss(){
            this.bol1 = true;
            this.val = $("input").val();
            localStorage.val = this.val;
            console.log(localStorage.val);
            this.arr.push(localStorage.val);
            console.log(this.arr);
            if(document.getElementsByTagName("input")[0].value==""){
                 alert("您输入的内容为空");
                 return false;
            }else{
                $("input").val("");
                this.$router.push("/chuncai");
            }
          },
          zz(){
            this.bol = true;
          },
          chuchu(){
            $(".suo").remove();
          },
          s(){
            this.bol1 = true;
          }
        }


    }
</script>

<style scoped>
  *{
    margin: 0;
    padding: 0;
  }
  .wrap{
    width: 100%;
    background-color: #f2f2f2;
  }
  .top{
    display: flex;
    justify-content:space-between;
    background-color: red;
    height: 11.3rem;
    line-height: 11.3rem;
    width: 100%;
  }
  .top img:nth-child(1){
    width: 2.3rem;
    height: 3.8rem;
    margin-top:3.7rem;
    margin-left: 2rem;
  }
  .fx{
    margin-top: 1rem;
    margin-right: 2rem;
    font-size: 3rem;
    color: #fff;
  }
  .top div{
    text-align: center;
    width: 54.3rem;
    height: 6rem;
  }
  .top div input{
    margin-left: -1rem;
    width: 54.3rem;
    height: 6rem;
    border-radius: 1rem;
    font-size: 2.4rem;
  }
  input::-webkit-input-placeholder {
    /* placeholder颜色  */
    color: #e53e42;
    /* placeholder字体大小  */
    font-size: 2.4rem;
    /* placeholder位置  */
    text-align: left;
  }
  .sousuo{
    width: 2.8rem;
    height: 3rem;
    position: absolute;
    left: 8rem;
    top: 4rem;
  }
  .bb{
    height: 8rem;
    line-height: 8rem;
  }
  .bb p{
    font-size: 2.8rem;
    margin-left: -55rem;
    color: #808080;
  }
  .bc{
    display: flex;
    justify-content: left;
    background-color: #fff;
    padding-top: 2rem;
    padding-bottom: 1rem;
  }
  .bc button{
    background: #fff;
    border: 1px solid gray;
    border-radius: 2rem;
    width: 13rem;
    height: 4rem;
    margin-left: 2rem;
    font-size: 2.8rem;
  }
  .suo{
    margin-top: 10rem;
    text-align: left;
    background-color: #fff;
  }
  .suo p{
    font-size: 2.8rem;
    margin-left: 2rem;
    color: #dedede;
    height: 6rem;
    line-height: 6rem;
  }
  .ul1{
    list-style-type: none;
    background-color: #fff;
  }
  .ul1 li{
    font-size: 2.8rem;
    margin-left: 2rem;
    border-bottom: 1px solid #ccc;
    height: 8rem;
    line-height: 8rem;
  }
  .suo button{
    width: 50.1rem;
    height: 4rem;
    border-radius: 2rem;
    margin-left: 10rem;
    font-size: 2.4rem;
    background-color: #fff;
    color: #ccc;
    border: 1px solid #ccc;
  }
</style>
