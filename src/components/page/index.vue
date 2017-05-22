<template>
  <div class="panel">
  <div class="block">
    <!-- <span class="demonstration">默认 Hover 指示器触发</span> -->
    <el-carousel height="350px">
      <el-carousel-item v-for="(list,item) in slideList" :key="item">
        <img :src="list.image" :alt="list.desc">
      </el-carousel-item>
    </el-carousel>
  </div>
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

</div>
</template>

<style>
  /*.el-row {
    text-align: center;
  }*/
  
  .el-row {
    width:600px;
    margin:auto;
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
            "image": "../../../static/img/u508.png"
        },
        {
            "clickUrl": "#",
            "desc": "hxrj",
            "image": "../../../static/img/u512.png"
        },
        {
            "clickUrl": "#",
            "desc": "rsdh",
            "image": "../../../static/img/u516.png"
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
