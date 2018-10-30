<template>
    <div>
         <div class="form-control">
            <div class="label require">服务：</div>
            <div class="service-wrap">
            <span class="service" v-for="(item,index) in service" :key="index" :class="index == 1 ? 'select-service' : ''">{{item}}</span>
        </div>
        </div>
        <div class="form-control">
            <div class="label require">职业：</div>
            <input type="text" class="ipt">
        </div>
        <div class="form-control">
            <div class="label require">工作年限：</div>
            <div class="service-wrap">
            <span class="service" v-for="(item,index) in work_year" :key="index">{{item}}</span>
            </div>
        </div>
        <div class="form-control">
            <div class="label require">项目地址：</div>
            <input type="text" class="ipt">
            <span class="add-project">+</span>
        </div>
        <div class="form-control">
            <div class="label require">博客地址：</div>
            <input type="text" class="ipt">
        </div>
        <div class="form-control">
            <button class="btn" @click="nextStep">下一步</button>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
            service: ["设计","摄影","H5","网站开发","小程序"],
            work_year: ["1年","2年","3-5年"]
            }
        },
        created() {
            
        },
        methods: {
            nextStep() {
                this.$router.push({path:"/join/join/step:two?step=2"});
            }
        }
    }
</script>
