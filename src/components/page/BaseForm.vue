<template>
  <div class="panel">
    <div class="white-panel">
        <div class="crumbs">
            <el-breadcrumb separator="/">
                <el-breadcrumb-item><i class="el-icon-date"></i> 订单</el-breadcrumb-item>
                <el-breadcrumb-item>基本表单</el-breadcrumb-item>
            </el-breadcrumb>
        </div>
        <div class="form-box">
            <el-form ref="form" :model="form" label-width="80px">
                <el-form-item label="名称">
                    <el-input v-model="form.name"></el-input>
                </el-form-item>
                <el-form-item label="性别">
                    <el-radio-group v-model="form.gender">
                        <el-radio label="男"></el-radio>
                        <el-radio label="女"></el-radio>
                        <!-- <el-radio label="imoo"></el-radio> -->
                    </el-radio-group>
                </el-form-item>
                <el-form-item label="性别">
                    <el-select v-model="form.region" placeholder="请选择">
                        <el-option label="男" value="bbk"></el-option>
                        <el-option label="女" value="xtc"></el-option>
                        <!-- <el-option label="imoo" value="imoo"></el-option> -->
                    </el-select>
                </el-form-item>
                <el-form-item label="日期时间">
                    <el-col :span="11">
                        <el-date-picker type="date" placeholder="选择日期" v-model="form.date1" style="width: 100%;"></el-date-picker>
                    </el-col>
                    <el-col class="line" :span="2">-</el-col>
                    <el-col :span="11">
                        <el-time-picker type="fixed-time" placeholder="选择时间" v-model="form.date2" style="width: 100%;"></el-time-picker>
                    </el-col>
                </el-form-item>
                <el-form-item label="价格">
                    <el-input type="textarea" v-model="form.price"></el-input>
                </el-form-item>
                <el-form-item label="地点">
                    <el-input type="textarea" v-model="form.position"></el-input>
                </el-form-item>
                <!-- <el-form-item label="选择开关">
                    <el-switch on-text="" off-text="" v-model="form.delivery"></el-switch>
                </el-form-item> -->
                <el-form-item label="风格">
                    <el-checkbox-group v-model="form.type">
                        <el-checkbox label="可爱" name="type"></el-checkbox>
                        <el-checkbox label="日系" name="type"></el-checkbox>
                        <el-checkbox label="阳光" name="type"></el-checkbox>
                    </el-checkbox-group>
                </el-form-item>

                <el-form-item label="说明">
                    <el-input type="textarea" v-model="form.desc"></el-input>
                </el-form-item>
                <el-form-item>
                    <el-button type="primary" @click="onSubmit">提交</el-button>
                    <el-button>取消</el-button>
                </el-form-item>
            </el-form>
        </div>

    </div>
  </div>
</template>

<script>
    export default {
        data: function(){
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
                    position:''
                }
            }
        },
        methods: {
            onSubmit() {
                this.$message.success('提交成功！');
            }
        }
    }
</script>
