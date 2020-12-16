<template>
    <div id="home">
      <div class="title">
        <div class="left">
          <img src="../../assets/img/icon4.png" alt="">
        </div>
        <div class="center">
           <span>平安成电智慧通行</span>
        </div>
        <div class="right">
          <ul>
            <li></li>
            <li></li>
            <li></li>
          </ul>
        </div>
      </div>
      <div class="top">
        <div class="isgo">
           <span v-html="message"></span>
        </div>
        <div class="info">
          <div class="user-info">
            <div class="id1">
              <img src="../../assets/img/icon1.png" alt="">
              <span>用户姓名</span>
            </div>
            <div class="id2">{{username}}</div>
          </div>
          <div class="reg-type">
            <div class="id1">
              <img src="../../assets/img/icon2.png" alt="">
              <span>登记类型</span>
            </div>
            <div class="id2 stu">
              研究生(硕士)
            </div>
          </div>
          <div class="reg-time">
            <div class="id1">
              <img src="../../assets/img/icon3.png" alt="">
              <span>登记时间</span>
            </div>
            <div class="id2 time">
              <home-swiper></home-swiper>
            </div>
          </div>
        </div>
        <div class="button">
          前往个人二维码
        </div>
        <div class="logo">
          <img src="https://smaco2.uestc.edu.cn/img/bwc_wechat.d6141ed0.png" alt="">
        </div>
      </div>
      <input type="text" v-model="username" v-show="username==''">
    </div>
</template>

<script>
import HomeSwiper from './HomeSwiper'
export default {
  name: 'Home',
  components: {
    HomeSwiper
  },
  data(){
    return {
      username: '',
      isShow: true,
      message: "研究生用户，入校授权有效"
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#home{
  height: 800px;
  /* margin-top: 48px; */
  font-family: "Helvetica Neue",Helvetica,"PingFang SC","Hiragino Sans GB","Microsoft YaHei","微软雅黑",Arial,sans-serif;
  background-color: #fafafa;
}
.title{
  height: 55px;
  line-height: 50px;
  display: flex;
  font-weight: 540;
  background-color: #fff;
  justify-content: space-between;
}

.center span {
  padding-bottom: 4px;
  font-size: 17px;
  font-weight: 600;
  color: #333;
}
.right ul li {
  float: left;
  padding-right: 10px ;
}
.top {
  background-color: #fff;
}
.isgo{
  padding: 60px 16px 30px 16px;
  height: 36px;
  line-height: 36px;
  text-align: justify;
  /* margin: 16px 0; */
}
.isgo span {
  font-weight: bold;
  color: green;
  font-size: 24px;
  width: 100%;
  display: inline-block;
}
.info{
  padding: 8px 0;
  width: 100%;
  font-weight: 400;
  font-size: 16px;
  border-top: 1px solid rgba(0,0,0,.12);
  margin-bottom: 10px
}

.user-info,
.reg-type,
.reg-time {
   padding: 0 15px;
   height: 48px;
   line-height: 48px;
   display: flex;
   justify-content: space-between;
} 
.id1 {
  font-family: Roboto,Noto Sans S Chinese,PingFangSC,Microsoft YaHei,sans-serif;
  color: #333;
  font-size: 16px;
}
.id2{
  font-size: 25px;
  font-weight: 700;
}
.id2.stu{
  padding-right: 25px;
}
.id2.time {
  width: 200px;
  text-align: right;
  color: #00c4a4;
  font-size: 18px;
  font-weight: 700;
}
.logo{
  padding: 20px 0 10px 0;
  text-align: center;
  margin: auto;
}
.logo img{
  height: 50px;
  width: 50px;
}
.id1 img {
  margin-top: -3px;
  width: 35px;
  height: 30px;
  vertical-align: middle;
}
.button{
  margin: auto;
  width: 150px;
  height: 50px;
  color: #fff;
  text-align: center;
  line-height: 50px;
  border-radius: 5px;
  background-color: #39ccb3;
}
</style>
