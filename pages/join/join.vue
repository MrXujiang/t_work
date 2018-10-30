<template>
  <section class="join-container">
    <div class="title">申请成为服务商</div>
    <div class="form-wrap">
      <div class="step-wrap">
        <div class="step step-one current">1</div>
        <div :class="['step', 'step-two', isStep_two ? 'current' : '']">2</div>
      </div>
      <nuxt-child />
    </div>
  </section>
</template>

<script>
import './join.less'

export default {
  asyncData({ query }) {
    let isStep_two = (query.step == 2);
    return {
      isStep_two
    }
  },
  components: {
      
  },
  data() {
    return {
      
    }
  },

  watch: {
      // 动态监听路由变化，重新渲染数据
      '$route' (to, from) {
        let { query } = to;
            this.isStep_two = query.step == 2;
      }
  }
}
</script>

