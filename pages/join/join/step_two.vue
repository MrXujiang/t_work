<template>
    <div>
         <div class="form-control">
            <div class="label require">姓名：</div>
            <input type="text" class="ipt">
        </div>
        <div class="form-control">
            <div class="label require">手机号：</div>
            <input type="text" class="ipt">
        </div>
        <div class="form-control">
            <div class="label require">验证码：</div>
            <input type="text" class="ipt ipt-sm">
            <span class="code">获取验证码</span>
        </div>
        <div class="form-control">
            <div class="label require">身份证号：</div>
            <input type="text" class="ipt">
        </div>
        <div class="form-control">
            <div class="label require">证件上传：</div>
            <div class="example">
                <div class="photo">
                    <div class="img-wrap"><img src="~/assets/images/face.png" alt=""></div>
                    <div class="example-tip">正面参考</div>
                    <div class="upload">
                        <label for="face" class="upload-btn gray">
                            正面上传<input type="file" class="ipt-file" id="face">
                        </label>
                    </div>
                </div>
                <div class="photo">
                    <div class="img-wrap"><img src="~/assets/images/oppsite.png" alt=""></div>
                    <div class="example-tip">反面参考</div>
                    <div class="upload">
                        <label for="opposite" class="upload-btn">
                            反面上传<input type="file" class="ipt-file" id="opposite">
                        </label>
                    </div>
                </div>    
            </div>
        </div>
        <div class="form-control">
            <button class="btn gray" @click="prevStep">上一步</button>
            <button class="btn">提交</button>
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
        methods: {
            prevStep() {
                this.$router.push({path:"/join/join"});
            }
        }
    }
</script>
