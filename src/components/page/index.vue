<template>
  <div class="panel">
  <div class="block">
    <!-- <span class="demonstration">默认 Hover 指示器触发</span> -->
    <el-carousel height="350px">
      <el-carousel-item v-for="(list,item) in slideList" :key="item" :interval="5000">
        <img :src="list.image" :alt="list.desc">
      </el-carousel-item>
    </el-carousel>
  </div>
  <!--
  <div class="white-panel">
  <el-row >
  <el-col  :span="8" v-for="(o, index) in 2" :key="o" :offset="index > 0 ? 2 : 0">
    <el-card :body-style="{ padding: '0px' }">
      <div >
        <img src="../../../static/img/img.jpg" class="image">
      </div>
      <div style="padding: 14px;">
        <span>好吃的汉堡</span>
        <div class="bottom clearfix">
          <time class="time">{{ currentDate }}</time>
          <el-button type="text" class="button" @click="jump">操作按钮</el-button>
        </div>
      </div>
    </el-card>
  </el-col>
</el-row>
<el-dialog
  title="提示"
  :visible.sync="dialogVisible"
  size="tiny"
  :before-close="handleClose">
  <span>这是一段信息</span>
  <span slot="footer" class="dialog-footer">
    <el-button @click="dialogVisible = false">取 消</el-button>
    <el-button type="primary" @click="dialogVisible = false">确 定</el-button>
  </span>
</el-dialog>

</div>
-->
<div class="panel">
<el-row class="bg-normal">
<el-col :span="5" >
<div class="grid-content bg-normal"></div>
</el-col>
<el-col :span="6">
<div class="grid-content bg-gray">
  <a href=""><img src="../../../static/img/index/u529_mouseOver.png" class="font-img img-special">
  <div class="font-content">我要</div>
  <div class="font-content">找摄影师</div>
  </a>
</div>
</el-col>
<el-col :span="2">
<div class="grid-content bg-normal"></div>
</el-col>
<el-col :span="6">
<div class="grid-content bg-gray">
  <a href="">
    <img src="../../../static/img/index/u531_mouseOver.png" class="font-img">
  <div class="font-content">我要</div>
  <div class="font-content">找模特</div>
  </a>
</div>
</el-col>
<el-col :span="5">
<div class="grid-content bg-normal"></div>
</el-col>
</el-row>
</div>

<div class="panel">
  <el-row class="bg-white">
  <div class="font-num3">咔嚓摄影，定格的不只是时光</div>
  <div class="font-num4">四大优势，您首选的约拍平台</div>
  <el-col :span="4">
  </el-col>
  <el-col :span="4">
  <img src="../../../static/img/index/u555.png" class="font-img img-special">
  <div class="font-num1">专业摄影</div>
  <div class="font-num2">平台签约校园摄影师</div>
  <div class="font-num2">专业摄影只为您服务</div>
  </el-col>
  <el-col :span="4">
  <img src="../../../static/img/index/u557.png" class="font-img img-special">
  <div class="font-num1">个性定制</div>
  <div class="font-num2">专业只为您量身定制</div>
  <div class="font-num2">你就是不一样的烟火</div>
  </el-col>
  <el-col :span="4">
    <img src="../../../static/img/index/u559.png" class="font-img img-special">
  <div class="font-num1">服务到位</div>
  <div class="font-num2">线上下单线下拍摄</div>
  <div class="font-num2">服务跟踪完美售后</div>
  </el-col>
  <el-col :span="4">
      <img src="../../../static/img/index/u561.png" class="font-img img-special">
  <div class="font-num1">安全无忧</div>
  <div class="font-num2">认证商家服务保障</div>
  <div class="font-num2">规则清晰监管完善</div>
  </el-col>
  <el-col :span="4">
  </el-col>
  </el-row>
</div>
</div>
</template>

<style>
  /*.el-row {
    text-align: center;
  }*/

 .panel{
  background-color: white;
 }
  .el-row {
    text-align: center;
    width:100%;
    height: auto;
    margin-bottom: 0px;

  }
  .el-col{
    margin-top: 30px;
    margin-bottom: 30px;
  }
 .grid-content{
  border-radius: 4px;
  min-height: 36px;
  height: 250px;
 }
 .bg-gray{
  background-color: #ADADAD;
 }
 .bg-normal{
  background-color: #EAEAEA;
 }
 .bg-white{
  background-color: white;
 }
 .font-img{
  margin-top: 15px;
  height: 110px;
 }
 .img-special{
   height: 90px;
   margin-top: 25px;
   margin-bottom: 10px;
 }
 .font-content{
  color: white;
  font-size: 200%;
  margin-top: 5px;
 }
 .font-num1{
  font-size: 120%;
  margin-bottom: 8px;
 }
  .font-num2{
  font-size: 80%;
  margin-bottom: 8px;
 }
   .font-num3{
  font-size: 200%;
  margin-top: 20px;
  margin-bottom: 10px;
 }
   .font-num4{
  font-size: 110%;
  margin-top: 10px;
  margin-bottom: 10px;
 }
  .el-carousel__item img {
   width:100%;
  }

  .time {
    font-size: 13px;
    color: #999;
  }

  .bottom {
    margin-top: 13px;
    line-height: 12px;
  }

  .button {
    padding: 0;
    float: right;
  }

  .image {
    width: 100%;
    display: block;
  }

  .clearfix:before,
  .clearfix:after {
      display: table;
      content: "";
  }

  .clearfix:after {
      clear: both
  }
  /*.cardtop {
    height:40px;
    overflow-y: hidden;
  }*/
  /*.el-col-offset-2 {
    margin-left: 0;
}*/

</style>
<script>
export default {
  data() {
    return {
      currentDate: new Date(),
      dialogVisible: false,
      slideList: [
        {
            "clickUrl": "#",
            "desc": "nhwc",
            "image": "../../../static/img/index/u508.png"
        },
        {
            "clickUrl": "#",
            "desc": "hxrj",
            "image": "../../../static/img/index/u512.png"
        },
        {
            "clickUrl": "#",
            "desc": "rsdh",
            "image": "../../../static/img/index/u516.png"
        }
    ]
    };

  },
  methods: {
      handleClose(done) {
        this.$confirm('确认关闭？')
          .then(_ => {
            done();
          })
          .catch(_ => {});
      },
      jump(){
        this.$router.push('/Carousel');
      }
    }
}
</script>
