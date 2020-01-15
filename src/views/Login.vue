<template>
    <div class="form">

      <el-radio-group v-model="selectedTag" size="small">
        <el-radio-button label="登陆"></el-radio-button>
        <el-radio-button label="注册"></el-radio-button>
      </el-radio-group>

      <el-form v-if="selectedTag==='登陆'" label-position="left" label-width="80px">
        <el-form-item label="用户名">
          <el-input></el-input>
        </el-form-item>
        <el-form-item label="密码">
          <el-input></el-input>
        </el-form-item>
        <el-form-item label="验证码">
          <el-input></el-input>
        </el-form-item>
        <el-form-item>
          <el-button @click="checkLogin">登陆</el-button>
        </el-form-item>
      </el-form>

      <el-form v-else label-position="left" label-width="80px">
        <el-form-item label="用户名">
          <el-input></el-input>
        </el-form-item>
        <el-form-item label="密码">
          <el-input></el-input>
        </el-form-item>
        <el-form-item label="确认密码">
          <el-input></el-input>
        </el-form-item>
        <el-form-item>
          <el-button>注册</el-button>
        </el-form-item>
      </el-form>
    </div>
</template>

<script>
export default {
  name: 'login',
  data() {
    return {
      selectedTag: '登陆'
    };
  }
};
</script>

<style lang="scss" scoped>

$body-bg: #c1bdba;
$form-bg: #13232f;
$white: #ffffff;

$main: #1ab188;
$main-light: lighten($main,5%);
$main-dark: darken($main,5%);

$gray-light: #a0b3b0;
$gray: #ddd;

$thin: 300;
$normal: 400;
$bold: 600;
$br: 4px;

.form {
  background:rgba($form-bg,.9);
  padding: 40px;
  max-width:600px;
  margin:40px auto;
  border-radius:$br;
  box-shadow:0 4px 10px 4px rgba($form-bg,.3);
}
</style>
