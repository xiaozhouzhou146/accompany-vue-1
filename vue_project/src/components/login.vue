<template>
  <div class="wrap">
    <div class="Img"><img src="../assets/3.png" /></div>
    <ul class="container">
      <li class="showImg"></li>
      <li class="login">
        <div class="loginText">登录</div>
        <div class="loginPhone">
          <div>+86</div>
          <input type="text" placeholder="输入手机号" />
          <div style="margin: 20px 0" class="btn">
            <button>验证码</button>
          </div>
        </div>
        <div class="loginVerfiy">
          <input type="text" placeholder="输入验证码" />
        </div>
        <!-- <div class="loginVerfiy">
          <el-select v-model="value4" placeholder="请选择" size="small">
            <el-option
              v-for="item in options"
              :key="item.value"
              :label="item.label"
              :value="item.value"
            >
            </el-option>
          </el-select>
        </div> -->
        <div class="submit">
          <button>登录</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "loginView",
  data() {
    return {
    //   options: [
    //     {
    //       value: "1",
    //       label: "病人",
    //     },
    //     {
    //       value: "2",
    //       label: "陪诊师",
    //     },
    //   ],
    //   value4: "病人",
    };
  },
}
</script>

<style>
body {
  background-color: #222;
}

* {
  list-style: none;
}
.wrap {
  position: relative;
}
.Img {
  position: absolute;
  top: 40px;
  left: 50%;
  transform: translateX(-50%);
}
.Img img {
  width: 70%;
}
.container {
  position: absolute;
  width: 600px;
  height: 300px;
  top: 120px;
  left: 50%;
  transform: translateX(-50%);
  border-radius: 25px;
  background-color: #fff;
  /* overflow: hidden; */
}
.container li {
  float: left;
}
.login {
  width: 47%;
  margin-right: -40px;
  height: 100%;
  /* background-color: skyblue; */
  border-top-right-radius: 25px;
  border-bottom-right-radius: 25px;
}
.loginPhone,
.loginVerfiy,
.loginText,
.submit {
  width: 77%;
  /* background-color: red; */
  margin: 0 auto;
  text-align: center;
}
.loginText {
  margin-top: 30px;
  margin-bottom: 20px;
}
.showImg {
  height: 100%;
  width: 60%;
  margin-left: -40px;
  border-top-left-radius: 25px;
  border-bottom-left-radius: 25px;
  background-color: pink;
}
input {
  width: 210px;
  height: 30px;
  outline: none;
  border: none;
  border-bottom: solid #000 1px;
  text-align: center;
}
.loginPhone div:nth-child(1) {
  position: absolute;
  top: 75px;
}
.btn {
  position: absolute;
  top: 50px;
  right: 0;
}

.btn button {
  position: absolute;
  right: 30px;
  height: 30px;
  width: 55px;
  border: none;
  background-color: white;
  color: peru;
}
.submit button {
  border: none;
  width: 220px;
  height: 40px;
  margin-top: 15px;
}
.loginVerfiy {
  height: 60px;
  line-height: 60px;
}
</style>