<template>
  <section class="container w">
    <div class="banner">
      <img src="~/assets/images/top_banner.png" alt="">
    </div>
    <div class="serach-wrap">
      <input type="text" placeholder="搜索需求" autofocus="autofocus">
      <div class="require-rank">
        需求排行榜：<span class="hot-require">小程序开发</span>
      </div>
    </div>
    <div class="main">
      <div class="require-wrap">
        <div class="require-cate">
          分类：
          <nuxt-link to="/require/project/" class="cate-nav">网站</nuxt-link>
          <nuxt-link to="/require/project?type=small_code" class="cate-nav">小程序</nuxt-link>
          <nuxt-link to="/require/project?type=H5" class="cate-nav">H5</nuxt-link>
          <nuxt-link to="/require/project?type=design" class="cate-nav">设计</nuxt-link>
          <nuxt-link to="/require/project?type=photograph" class="cate-nav">摄影</nuxt-link>
        </div>
        <div class="require-content">
          <nuxt-child />
        </div>
      </div>
      <div class="ad-wrap">
        <div class="ad">
          <img src="~/assets/images/ad1.jpg" alt="">
        </div>
        <div class="ad">
          <img src="~/assets/images/ad2.jpg" alt="">
        </div>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  components: {
      
  }
}
</script>

<style lang="less" scoped>
.container {
  min-height: 100vh;
  .banner {
    margin-top: 18px;
    width: 100%;
    img {
      width: 100%;
    }
  }

  .serach-wrap {
    margin-top: 30px;
    height: 176px;
    padding-top: 40px;
    padding-bottom: 40px;
    text-align: center;
    background-color: rgba(0,0,0,.11);

    ::-webkit-input-placeholder { /* WebKit browsers */
        color: #000;
        text-align: center; }
    :-moz-placeholder { /* Mozilla Firefox 4 to 18 */
        color: #000;
        text-align: center; }
    ::-moz-placeholder { /* Mozilla Firefox 19+ */
        color: #000;
        text-align: center; }
    :-ms-input-placeholder { /* Internet Explorer 10+ */
        color: #000;
        text-align: center; }
    input:focus::-webkit-input-placeholder{ color:#000; text-align: center; }

    input {
      display: inline-block;
      width: 410px;
      border-bottom: 2px solid #000;
      font-size: 30px;
      line-height: 1.6em;
      text-align: center;
      background-color: transparent;
    }

    .require-rank {
      margin-top: 16px;
      .hot-require {
        color: #59a506;
      }
    }
  }

  .main {
    margin-top: 20px;
    display: flex;
    .require-wrap {
      flex: 1;
      .require-cate {
        margin-bottom: 40px;
        .cate-nav {
          display: inline-block;
          text-align: center;
          width: 80px;
        }
        .nuxt-link-exact-active {
          color: #59a506;
        }
      }
    }

    .ad-wrap {
      margin-left: 52px;
      .ad {
        width: 300px;
        margin-bottom: 20px;
        img {
          width: 100%;
        }
      }
    }
  }
}


</style>
