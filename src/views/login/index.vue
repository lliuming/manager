<template>
  <div class="login-div">
    <el-row type="flex" justify="center">
      <el-col><h3>管理系统</h3></el-col>
    </el-row>
    <el-row type="flex" justify="center">
      <el-col :md="10" :sm="10" :xs="20" :xl="6">
        <el-form :label-position="labelPosition" :rules="rules" label-width="80px" :model="loginForm" ref="loginForm">
          <el-form-item label="用户名" prop="userName">
            <el-input v-model="loginForm.userName"></el-input>
          </el-form-item>
          <el-form-item label="密码" prop="password">
            <el-input v-model="loginForm.password" type="password"></el-input>
          </el-form-item>
          <el-form-item>
            <el-row type="flex" justify="start">
              <el-col><el-button type="primary" @click="$_login_login">登陆</el-button></el-col>
              <el-col><el-button type="info" @click="$_login_reset">重置</el-button></el-col>
            </el-row>
          </el-form-item>
        </el-form>
      </el-col>
      <!-- <el-col :span="8"><div class="grid-content bg-purple"></div></el-col>
      <el-col :span="8"><div class="grid-content bg-purple"></div></el-col> -->
    </el-row>
    <!-- <el-row type="flex" :gutter="20">
      <el-col :span="24"><div class="grid-content bg-purple"></div></el-col>
    </el-row>
    <el-row type="flex" :gutter="20">
      <el-col :span="24"><div class="grid-content bg-purple"></div></el-col>
    </el-row> -->
  </div>
</template>
<script>
export default {
  data() {
    return {
      labelPosition: 'left',
      loginForm: {
        userName: '',
        password: ''
      },
      rules: {
        // userName: [
        //   { required: true, message: '请输入用户名称', trigger: 'blur' }
        // ]
      }
    }
  },
  methods: {
    $_login_login() {
      
    },
    $_login_reset() {
      // 重置要要写prop，otherwise无效
      this.$refs.loginForm.resetFields();
    }
  }
}

</script>
<style scoped>
  .login-div {
    margin-top: 10%;
  }
  .el-row {
    margin-bottom: 20px;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .bg-purple {
    background: #d3dce6;
  }
</style>