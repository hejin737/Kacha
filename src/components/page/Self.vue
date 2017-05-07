<template>
<div class="panel">
    <div class="white-panel">



        <div class="crumbs">
            <el-breadcrumb separator="/">
                <el-breadcrumb-item><i class="el-icon-date"></i> 资料</el-breadcrumb-item>
                <el-breadcrumb-item>个人资料</el-breadcrumb-item>
            </el-breadcrumb>
        </div>
        <el-card class="box-card">
            <div slot="header" class="clearfix">
                <span style="line-height: 36px;">个人资料</span>
                <el-button style="float: right;" type="primary" @click="modify = !modify">
                  <span v-if="modify">修改</span>
                  <span v-else>保存</span>
                </el-button>
            </div>
            <div class="text item">
              <span>昵称：</span>
              <span v-if="modify">{{self.name }}</span>
              <input v-else v-model = "self.name">
            </div>
            <div class="text item">
              <span>所在地：</span>
              <span v-if="modify">{{self.position }}</span>
              <input v-else v-model = "self.position">
            </div>
            <div class="text item">
              <span>学校：</span>
              <span v-if="modify">{{self.school }}</span>
              <input v-else v-model = "self.school">
            </div>
            <!-- <div v-for="o in 4" :key="o" class="text item">
                {{'列表内容 ' + o }}
            </div> -->
        </el-card>


    </div>
</div>
</template>
<style>
.text {
    font-size: 14px;
}

.item {
    padding: 18px 0;
}

.clearfix:before,
.clearfix:after {
    display: table;
    content: "";
}

.clearfix:after {
    clear: both
}

.box-card {
    width: 90%;
    margin: auto;
}
</style>
<script>
export default {
    data: function() {
        return {
            form: {
                name: '订单名称',
                region: '',
                date1: '',
                date2: '',
                price: '',
                delivery: true,
                type: ['可爱'],
                gender: '女',
                desc: '',
                position: ''
            },
            self:{
              name:'haha',
              position:'上海',
              school:'上海交通大学'
            },
            modify:true,

        }
    },
    methods: {
        onSubmit() {
            this.$message.success('提交成功！');
        }
    }
}
</script>
