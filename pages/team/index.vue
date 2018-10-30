<template>
  <section class="w">
    <div class="team">
      <div class="tit green">
        设计团队
      </div>
      <div class="team-mumber">
        <div class="avator">
          <div v-for="(item,index) in team.designer" :key="index"><img src="~/assets/images/joiner.png" alt=""></div>
          <div><div class="team-num linear-green">999+</div></div>
        </div>
      </div>
    </div>
    <div class="team">
      <div class="tit blue">
        技术团队
      </div>
      <div class="team-mumber">
        <div class="avator">
          <div v-for="(item,index) in team.designer" :key="index"><img src="~/assets/images/joiner.png" alt=""></div>
          <div><div class="team-num linear-blue">999+</div></div>
        </div>
      </div>
    </div>
    <div class="team">
      <div class="tit purple">
        摄影师团队
      </div>
      <div class="team-mumber">
        <div class="avator">
          <div v-for="(item,index) in team.designer" :key="index"><img src="~/assets/images/joiner.png" alt=""></div>
          <div><div class="team-num linear-purple">999+</div></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import data from '~/data';

export default {
  components: {
      
  },
  asyncData() {

  },

  data() {
    return {
      team: {
        designer: [],
        engineer: [],
        cameraman: []
      }
    }
  },

  created() {
    // mock数据
    for(let i=0; i< 10; i++) {
      this.team.designer.push(data.teams.designer[0]);
      this.team.engineer.push(data.teams.designer[0]);
      this.team.cameraman.push(data.teams.designer[0]);
    }
  }
}
</script>

<style lang="less" scoped>
@green: #37dc83;
@blue: #31b0c6;
@purple: #9642dd;

.team {
  margin-bottom: 40px;
  .tit {
    margin-top: 40px;
    margin-bottom: 50px;
    font-size: 48px;
    text-align: center;
    &::before,
    &::after {
      content: '';
      display: inline-block;
      width: 4em;
      height: 4px;
      vertical-align: 15px;
    }
  }

  .team-mumber {
    .avator {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      div {
        margin-bottom: 40px;
        width: 15%;
        text-align: center;
        cursor: pointer;
        img, .team-num {
          width: 120px;
          height: 120px;
          border-radius: 50%;
        }

        .team-num {
          display: inline-block;
          color: #fff;
          font-size: 30px;
          line-height: 120px;
        }

        .linear-green {
          background: linear-gradient(-45deg, #2cc9a1, #54e58d);
        }

        .linear-blue {
          background: linear-gradient(-45deg, #36acce, #14d7d9);
        }

        .linear-purple {
          background: linear-gradient(-45deg, #9642dd, #e53de3);
        }
      }
    }
  }
}

.green {
  color: @green;
  &::before,
  &::after {
    background-color: @green;
  }
}

.blue {
  color: @blue;
  &::before,
  &::after {
    background-color: @blue;
  }
}

.purple {
  color: @purple;
  &::before,
  &::after {
    background-color: @purple;
  }
}

</style>
