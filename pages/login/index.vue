<template>
  <section class="container">
    <div class="form-wrap">
      <div class="form-tit">{{isLogin ? '登录' : '注册'}}</div>
      <div class="form-control">
        <input type="text" placeholder="用户名" autofocus="autofocus" v-if="isLogin" key="login_user">
        <input type="text" placeholder="用户名" autofocus="autofocus" v-else key="register_user">
      </div>
      <div class="form-control">
        <input type="password" placeholder="密码" key="login_psw" v-if="isLogin">
        <input type="password" placeholder="密码" key="register_psw" v-else>
      </div>
      <div class="form-control" v-if="!isLogin">
        <input type="password" placeholder="确认密码">
      </div>
      <div class="form-control">
        <input type="button" :value="isLogin ? '登录' : '注册'">
      </div>
      <div class="form-tip" v-if="!isLogin">
        已有账号？ <span @click="handleLogin">立即登录</span>
      </div>
      <div class="form-tip" v-else>
        还没账号？ <span @click="handleRegister">立即注册</span>
      </div>
    </div>
    <div class="bg">
      <div class="bar green-bar"></div>
      <div class="bar blue-bar"></div>
      <div class="bar purple-bar"></div>
    </div>
    <div class="bg-txt">Welcome</div>
  </section>
</template>

<script>

export default {
  components: {
      
  },
  layout: 'login',
  data() {
    return {
      isLogin: true
    }
  },
  methods: {
    handleRegister () {
      this.isLogin = false;
    },
    handleLogin () {
      this.isLogin = true;
    }
  }
}
</script>

<style lang="less" scoped>
@greenHeight: 40px;
@green: #33d392;
@purpleHeight: 46px;
@purple: #8036d4;
@blueHeight: 40px;
@blue: #62bffd;

@hdHeght: 120px;

.container {
  flex: 1;

  .form-wrap {
    position: relative;
    z-index: 1;
    width: 340px;
    margin-top: 40px;
    margin-left: auto;
    margin-right: 242px;
    padding: 20px 34px;
    border-radius: 6px;
    text-align: center;
    background-color: #fff;
    box-shadow: 0 0 20px rgba(0,0,0,.2);

    .form-tit {
      margin-bottom: 40px;
      color: #ccc;
      font-weight: bold;
    }

    .form-control {
      margin-bottom: 40px;

      ::-webkit-input-placeholder { /* WebKit browsers */
          color: #ccc;
          text-align: center; }
      :-moz-placeholder { /* Mozilla Firefox 4 to 18 */
          color: #ccc;
          text-align: center; }
      ::-moz-placeholder { /* Mozilla Firefox 19+ */
          color: #ccc;
          text-align: center; }
      :-ms-input-placeholder { /* Internet Explorer 10+ */
          color: #ccc;
          text-align: center; }
      input:focus::-webkit-input-placeholder{ color:#ccc; text-align: center; }

      // 修改表单自动完成样式
      input:-webkit-autofill, textarea:-webkit-autofill, select:-webkit-autofill,
      input:-webkit-autofill:hover, input:-webkit-autofill:focus {
        -webkit-box-shadow: 0 0 0px 1000px white inset,
                            0 1px #f2f1f3;
        color: rgb(0, 0, 0);
      }

      input {
        display: block;
        width: 100%;
        line-height: 2em;
        text-align: center;
        box-shadow: 0 1px #f2f1f3;
        caret-color: #8036d4;
      }

      input[type="button"] {
        height: 46px;
        border-radius: 27px;
        color: #fff;
        text-align: center;
        cursor: pointer;
        background-color: #8036d4;
      }

      input[type="button"]:hover {
        background-color: #933cf7;
      }
    }

    .form-tip {
      font-size: 14px;
      color: #656466;
      span {
        cursor: pointer;
      }
    }
  }

  .bg {
    position: absolute;
    top: 0;
    height: 100vh;
    width: 100%;

    .bar {
      position: absolute;
      height: @greenHeight;
    }

    .green-bar {
      left: 220px;
      top: @hdHeght;
      margin-top: 40px;
      width: 56px;
      border-radius: @greenHeight / 2;
      background-color: @green;
      &::after,
      &::before {
        content: '';
        position: absolute;
        display: inline-block;
        border-radius: @greenHeight / 2;
        background-color: @green;
      }

      &::after {
        height: @greenHeight;
        width: 296px;
        margin-left: 86px;
      }

      &::before {
        left: 0;
        height: 70%;
        width: 296px;
        margin-left: -296px;
        margin-top: 170px;
        transform: rotate(-45deg);
        box-shadow: -90px 20px rgba(51,211,146,.2);
      }
    }

    .purple-bar {
      left: 320px;
      bottom: 60px;
      width: 500px;
      height: @purpleHeight;
      border-radius: @purpleHeight / 2;
      background-color: @purple;
      &::after,
      &::before {
        content: '';
        position: absolute;
        display: inline-block;
        border-radius: @purpleHeight / 2;
        background-color: @purple;
      }

      &::after {
        bottom: 0;
        left: 600px;
        transform: translateY(60px);
        width: 200px;
        height: 160px;
      }

      &::before {
        left: -400px;
        height: @purpleHeight;
        width: 296px;
      }
    }

    .blue-bar {
      top: @hdHeght;
      margin-top: 106px;
      transform: translateX(-100px);
      right: 0;
      width: 540px;
      height: @blueHeight;
      border-radius: @blueHeight / 2;
      background-color: @blue;
      &::after {
        content: '';
        position: absolute;
        right: -80px;
        width: 60px;
        height: @blueHeight;
        display: inline-block;
        border-radius: @blueHeight / 2;
        background-color: @blue;
      }
    }
  }

  .bg-txt {
      position: absolute;
      bottom:240px;
      left: 320px;
      font-size: 40px;
      font-weight: bold;
      color: #933cf7;
      -webkit-box-reflect: below -0.3em -webkit-linear-gradient(top, transparent, transparent 20%, rgba(128, 54, 212, 0.2))
    }
}


</style>
