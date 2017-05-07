<template>
    <div class="sidebar">

        <el-menu :default-active="onRoutes" class="el-menu-demo" mode="horizontal" theme="dark" unique-opened router>
            <div class="logo">KACHA摄影</div>
            <el-menu-item index="index">
                <i class="el-icon-setting"></i>首页
            </el-menu-item>
            <el-submenu index="2">
                <template slot="title"><i class="el-icon-menu"></i>找摄影师</template>
                <el-menu-item index="Carousel">摄影师</el-menu-item>
                <el-menu-item index="vuetable">套餐</el-menu-item>
            </el-submenu>
            <el-submenu index="3">
                <template slot="title"><i class="el-icon-date"></i>找模特</template>
                <el-menu-item index="Carousel">模特</el-menu-item>
                <el-menu-item index="vuetable">订单</el-menu-item>
                <!-- <el-menu-item index="markdown">markdown</el-menu-item>
                <el-menu-item index="upload">文件上传</el-menu-item> -->
            </el-submenu>
            <el-submenu index="4">
                <template slot="title"><i class="el-icon-star-on"></i>亲爱的{{username}}用户</template>
                <el-menu-item index="Self">我的资料</el-menu-item>
                <el-menu-item index="BaseTable">我的订单</el-menu-item>
                <el-menu-item index="baseform">发布订单</el-menu-item>
                <el-menu-item index="Login" v-on:click="handleCommand">退出登录</el-menu-item>
            </el-submenu>
            <!-- <div class="user-info">
                <el-dropdown trigger="click" @command="handleCommand">
                    <span class="el-dropdown-link">
                        <img class="user-logo" src="../../../static/img/img.jpg">
                        {{username}}
                    </span>
                    <el-dropdown-menu slot="dropdown">
                        <el-dropdown-item command="loginout">退出</el-dropdown-item>
                    </el-dropdown-menu>
                </el-dropdown>
            </div> -->
        </el-menu>
    </div>
</template>

<script>
    export default {
      data() {
          return {
              name: 'linxin'
          }
      },
        computed:{
            onRoutes(){
                return this.$route.path.replace('/','');
            },
            username(){
                let username = localStorage.getItem('ms_username');
                return username ;//? username : this.name;
            }

        },
        methods:{
            handleCommand() {

                    localStorage.removeItem('ms_username')


            }
        }
    }
</script>

<style scoped>
  .el-menu--dark {
    background-color: #272c2f;
  }
    .sidebar{
        display: block;
        /*position: absolute;*/
        text-align: center;
        /*width: 250px;*/
        width:100%;
        /*left: 0;*/
        top: 70px;
        /*bottom:0;*/
        background: #2E363F;
    }
    .sidebar > ul {
        height:100%;
    }
    .sidebar .logo {
      float: left;
      width:250px;
      text-align: center;
      line-height: 60px;
      font-size: 22px;
      /*line-height: 70px;*/
      color: #fff;
      margin: 0;
      padding: 0;
    }
    .user-info {
        float: right;
        padding-right: 50px;
        font-size: 16px;
        color: #fff;
    }
    .user-info .el-dropdown-link{
        position: relative;
        display: inline-block;
        padding-left: 50px;
        color: #fff;
        cursor: pointer;
        vertical-align: middle;
    }
    .user-info .user-logo{
        position: absolute;
        left:0;
        top:15px;
        width:40px;
        height:40px;
        border-radius: 50%;
    }
</style>
