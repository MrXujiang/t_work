<template>
  <div>
    <div class="require-item" v-for="(item, index) in info" :key="index" @click="toDetail(item.id)">
      <div class="tit">{{ item.tit }}<span class="publish-time">{{ item.publish_time }}</span></div>
      <div class="info-wrap">
        <div class="info">
          <div class="source">
            来源：<span class="author">{{ item.source }}</span><span class="identify" v-if="item.isR">R</span>
          </div>
          <div class="source">
            地点：<span class="location">{{ item.location }}</span>
          </div>
        </div>
        <div class="money">{{ item.price }}元</div>
      </div>
    </div>
  </div>
</template>

<script>
import data from '~/data'

export default {
  asyncData({ query, env, error }) {
    let info;
    if(data.project[query.type]) {
      info = data.project[query.type];
    } else {
      info = data.project['website'];
    }
    return {
      info
    }
  },

  data() {
    return {
      
    }
  },

  created() {
    
  },

  methods: {
    toDetail(id) {
      // this.$router.push({path: `/require/${id}`});
      window.open(`/require/${id}`);
    }
  },

  watch: {
    // 动态监听路由变化，重新渲染数据
    '$route' (to, from) {
      let { type } = to.query;
        if(data.project[type]) {
          this.info = data.project[type];
        } else {
          this.info = data.project['website'];
        }
      }
    }
}
</script>

<style lang="less" scoped>
  .require-item {
    margin-bottom: 20px;
    padding: 20px 26px;
    background-color: #fff;
    box-shadow: 0 0 20px rgba(146, 145, 145, 0.2);
    cursor: pointer;
    .tit {
      font-size: 24px;
      .publish-time {
        float: right;
        color: #d0cfcf;
        font-size: 16px;
      }
    }

    .info-wrap {
      display: flex;
      .info {
        flex: 1;
        .source {
          margin-top: 20px;
          color: #d0cfcf;
          .author, .location {
            color: #999797;
          }
          .identify {
            margin-left: 1em;
            display: inline-block;
            width: 22px;
            height: 22px;
            line-height: 1;
            border: 2px solid #59a506;
            border-radius: 50%;
            text-align: center;
            color: #59a506;
            cursor: pointer;
          }
        }
      }

      .money {
        margin-bottom: 10px;
        font-size: 32px;
        color: #d58080;
        align-self: flex-end;
      }
    }
  }

</style>
