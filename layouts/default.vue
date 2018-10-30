<template>
  <div class="layout">
    <Header>
        <div class="logo"><img src="~/assets/images/logo.png" alt="黎西工坊"></div>
        <div class="nav">
          <nuxt-link to="/" class="nav-link" exact>首页</nuxt-link>
          <nuxt-link to="/require/project" class="nav-link">需求市场</nuxt-link>
          <nuxt-link to="/team" class="nav-link">团队介绍</nuxt-link>
          <nuxt-link to="/join/join" class="nav-link">申请入驻</nuxt-link>
          <nuxt-link to="/publish" class="nav-link">发布 +</nuxt-link>
        </div>
        <div class="login">
          <nuxt-link to="/login" class="login-link">登录</nuxt-link>
        </div>
    </Header>
    <nuxt/>
    <Footer />
  </div>
</template>

<script>
  import Header from '~/components/header.vue';
  import Footer from '~/components/footer.vue';

  // 样式
  import '~/assets/common.css'

  export default {
  components: {
    Header,
    Footer
  }
}
</script>
<style scoped>
.layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background-color: #f4f4f4;
}

 .logo {
    margin-right: 100px;
  }

  .logo img {
    width: 80px;
  }

.nav {
    flex: 1;
  }

  .nav .nav-link {
    position: relative;
    display: inline-block;
    padding: 1.6em;
  }

  .nav .nav-link:hover::after,
  .nav .nuxt-link-active::after {
    content: '';
    display: inline-block;
    position: absolute;
    margin-top: 2em;
    left: 1.6em;
    width: 1em;
    height: 3px;
    border-radius: 3px;
    background-color: #09ffe5;
  }

  .nav .nav-link,
  .login-link {
    font-size: 16px;
    color: #fff;
  }
</style>
