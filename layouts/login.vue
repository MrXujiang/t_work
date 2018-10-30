<template>
  <div class="layout">
    <Header>
        <div class="logo"><img src="~/assets/images/logo.png" alt="黎西工坊"></div>
        <div class="txt">Work For Internet</div>
        <div class="login">
          <nuxt-link to="/" class="login-link">返回首页</nuxt-link>
        </div>
    </Header>
    <nuxt/>
  </div>
</template>

<script>
  import Header from '~/components/header.vue';

  // 样式
  import '~/assets/common.css'

  export default {
  components: {
    Header
  }
}
</script>
<style scoped>
.layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.logo img {
    width: 80px;
}

.txt {
    flex: 1;
}

.login-link {
    font-size: 16px;
    color: #fff;
  }
</style>
