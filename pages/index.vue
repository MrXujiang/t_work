<template>
  <section class="container">
    <div class="banner w">
      <img src="~/assets/images/banner.png" alt="" class="top-banner">
      <img src="~/assets/images/dot.png" alt="" class="dot-img dot1">
      <img src="~/assets/images/dot.png" alt="" class="dot-img dot2">
      <img src="~/assets/images/dot.png" alt="" class="dot-img dot3">
    </div>
    <div class="adv service w">
      <div class="tit">精致服务</div>
      <div class="service-list">
        <div class="service-item">网站开发</div>
        <div class="service-item">小程序</div>
        <div class="service-item">H5</div>
        <div class="service-item">设计摄影</div>
      </div>
    </div>
    <div class="adv adv-intro w">
      <div class="tit">优势介绍</div>
      <div class="adv-list">
        <div class="adv-item">
          <div class="adv-el">优势一</div>
          <div class="adv-txt">
            <div class="adv-tit">大流量</div>
            <div class="adv-desc">全平台流量精准匹配，30000+用户的首选服务平台</div>
          </div>
        </div>
        <div class="adv-item">
          <div class="adv-txt">
            <div class="adv-tit">高可靠</div>
            <div class="adv-desc">平台服务商均来自平台严格筛选，拒绝低素质服务入流</div>
          </div>
          <div class="adv-el">优势二</div>
        </div>
        <div class="adv-item">
          <div class="adv-el">优势三</div>
          <div class="adv-txt">
            <div class="adv-tit">精准营销</div>
            <div class="adv-desc">基于AI的精准匹配，让每一个需求都精准对接</div>
          </div>
        </div>
      </div>
    </div>
    <div class="join">
      <nuxt-link to="/join/join" class="release-btn"></nuxt-link>
      <nuxt-link to="/publish" class="apply-btn"></nuxt-link>
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
@primary: #42e27c;

.container {
  background-color: @mainColor;
  .banner {
    position: relative;
    height: 400px;
    .top-banner {
      max-width: 900px;
    }

    .dot-img {
      position: absolute;
      width: 138px;
    }

    .dot1 {
      right: 328px;
      top: 90px;
      width: 138px;
    }

    .dot2 {
      right: 165px;
      top: 244px;
      width: 66px;
    }

    .dot3 {
      right: 166px;
      top: 16px;
      width: 58px;
    }

    .dot1, .dot2, .dot3 {
      animation: drop-dot infinite 5s linear;
    }
  }

  .adv {
    margin-bottom: 120px;
    color: @primary;
    text-align: center;
    .tit {
      position: relative;
      font-size: 28px;
      margin-bottom: 88px;
      &::after {
        content: '';
        display: inline-block;
        position: absolute;
        width: 1.5em;
        height: 3px;
        left: 50%;
        transform: translateX(-50%);
        margin-top: 2em;
        border-radius: 4px;
        background-color: @primary;
      }
    }
  }

  .service-list {
    display: flex;
    justify-content: space-around;
    .service-item {
      width: 146px;
      height: 146px;
      line-height: 146px;
      font-size: 22px;
      background: url(~/assets/images/circle.png) no-repeat center center;
      background-size: contain;
    }
  }

  .adv-list {
    margin-left: auto;
    margin-right: auto;
    width: 800px;
    .adv-item {
      margin-top: 80px;
      margin-bottom: 80px;
      display: flex;
      align-items: center;
      .adv-el {
        width: 160px;
        height: 160px;
        line-height: 160px;
        border-radius: 50%;
        font-size: 30px;
        text-align: center;
        background-color: #fff;
        animation: wave infinite 2s;
      }

      .adv-txt {
        flex: 1;
        .adv-tit {
          font-size: 36px;
          color: #fff;
        }

        .adv-desc {
          line-height: 3em;
        }
      }
    }
  }

  .join {
    display: flex;
    justify-content: center;

    .release-btn,
    .apply-btn {
      width: 248px;
      height: 100px;
      background-repeat: no-repeat;
      background-position: center center;
      background-size: 70%;
      transition: transform .6s;
      &:hover {
        transform: translateY(-6px);
      }
    }

    .release-btn {
      background-image: url(~/assets/images/join_btn.png);
    }

    .apply-btn {
      background-image: url(~/assets/images/publish_btn.png);
    }
  }
}

@keyframes drop-dot {
  0% {
    opacity: 0;
  }

  40% {
    opacity: 1;
    transform: translate(-60px, 60px);
  }

  80% {
    opacity: 0;
    transform: translate(-120px, 120px);
  }

  100% {
    opacity: 0;
  }
}

@keyframes wave {
    0% {
        box-shadow: 0 0 0 0 rgba(245, 226, 226, 1), 0 0 0 0 rgba(250, 189, 189, 1);
    }
    50% {
        box-shadow: 0 0 0 20px rgba(245, 226, 226, .5), 0 0 0 0 rgba(250, 189, 189, 1);
    }
    100% {
        box-shadow: 0 0 0 40px rgba(245, 226, 226, 0), 0 0 0 20px rgba(245, 226, 226, 0);
    }
}

</style>
