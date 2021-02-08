<template>
  <div>
    <el-form :model="form" :rules="rules" ref="form" class="login-box">
      <h3 class="login-title">欢迎登陆</h3>
      <el-form-item label="账号" prop="name">
        <el-input type="text" placeholder="请输入用户名" v-model="form.name"></el-input>
      </el-form-item>
      <el-form-item label="密码" prop="password">
        <el-input type="password" placeholder="请输入密码" v-model="form.password"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="onSubmit('form')">登陆</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data(){
    return{
      form:{
        name: '',
        password: ''
      },
      rules: {
        name: [
          {required: true, message: "请输入用户名", trigger: 'blur'}
        ],
        password: [
          {required: true, message: "请输入密码", trigger: 'blur'},
          {min: 6, message: "密码长度至少6位", trigger: 'blur'}
        ]
      }
    }
  },
  methods: {
    onSubmit(formName) {
      this.$refs[formName].validate((valid) => {
        if(valid) {
          this.$axios.post('http://localhost:8081/api/login', this.form).then((res)=>{
            this.$router.push("/blogs")
          })
        } else {
          return false;
        }
      });
    }
  }

}
</script>

<style  scoped>
  .login-box{
    width: 350px;
    margin: 120px auto;
    border: 1px solid #DCDFE6;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 0 30px #DCDFE6;
  }
  .login-title{
    text-align: center;
  }
</style>
