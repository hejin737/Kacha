<template>
    <div class="footer">
    <el-row>
  <el-col :span="4">
  <div class="">
  </div>
  </el-col>
  <el-col :span="4">
  <div class="font-num1">了解咔嚓</div>
  <div class="font-num2">关于咔嚓</div>
  <div class="font-num2">平台规则</div>
  <div class="font-num2">常见问题</div>
  <div class="font-num2">联系我们</div>
  </el-col>
  <el-col :span="4">
   <div class="font-num1">服务分类</div>
  <div class="font-num2">找摄影师</div>
  <div class="font-num2">找模特</div>
  </el-col>
  <div class="font-num3">关注我们</div>
  <el-col :span="4">
  <img src="../../../static/img/index/u53.png" width="130" height="130">
  <div class="font-num2">新浪微博：咔嚓摄影</div>
  </el-col>
  <el-col :span="4">
 <img src="../../../static/img/index/u53.png" width="130" height="130">
 <div class="font-num2">微信公众号：咔嚓摄影</div>
  </el-col>
  <el-col :span="4">
  <div class="">
  </div>
  </el-col>
</el-row>
    </div>
</template>
<script>
    export default {
        data() {
            return {
               
            }
        },
        
        methods:{

                
     }       
        
    }
</script>
<style scoped>
    .footer {
        position: relative;
        box-sizing: border-box;
        width: 100%;
        height: 300px;
        font-size: 22px;
        color: white;
        background-color: #272c2f;
      
    }
    .el-row{
      
    }
    .font-num1{
        font-size: 100%;
        margin-top: 10px;
     margin-bottom: 10px;
    }
    .font-num2{
        color: #FFF5EE;
        font-size: 60%;
        margin: 0px;
        padding: 0px;
        margin-bottom: 10px;
    }
    .font-num3{
        position: relative;
        left:-110px;
        font-size: 100%;
        margin-top: 40px;
        margin-bottom: 0px;

    }
    .el-col img{

    }
</style>
