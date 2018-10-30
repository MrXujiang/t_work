<template>
    <div class="container w">
        <div class="sider">
            <div class="sider-nav">
                <nuxt-link to="/publish" class="nav-link">发布需求</nuxt-link>
            </div>
        </div>
        <div class="main">
            <div class="bread-wrap">
                发布需求
            </div>
            <div class="require-wrap">
                <div class="require-hd">需求信息</div>
                <div class="require-form">
                    <div class="form-control required">
                        <input type="text" class="ipt" placeholder="请输入需求名称">
                    </div>
                    <div class="form-control required">
                        <div class="ipt placeholder" @click="showType">请选择需求类型
                            <div class="select-box" v-show="isShowType">
                                <div class="type">H5</div>
                                <div class="type">网站开发</div>
                                <div class="type">小程序</div>
                                <div class="type">设计</div>
                                <div class="type">摄影</div>
                            </div>
                        </div>
                    </div>
                    <div class="form-control required">
                        <div class="textarea-box">
                            <textarea placeholder="请输入需求简介"></textarea>
                        </div>
                    </div>
                    <div class="form-control required">
                        <input type="text" class="ipt" placeholder="请输入提供价格">
                    </div>
                    <div>
                        
                    <div class="upload-hd">上传图片<span class="file-tip">(注：不要在图片上放置设计师商业推广信息（除案例信息外），不超过100张，支持批量上传)</span></div>
                    <div class="form-control required">
                        <div class="file-box">
                            <label for="file_img"><input type="file" class="ipt-file" id="file_img"></label>
                        </div>
                    </div>
                    <div class="form-control required">
                        <input type="text" class="ipt" placeholder="请输入需求周期">
                    </div>
                    </div>
                </div>
                <div class="require-ft">
                    <button class="btn">发布</button>
                    <button class="btn gray">预览</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                isShowType: false
            }
        },
        methods: {
            showType() {
                this.isShowType = !this.isShowType;
            }
        }
    }
</script>

<style scoped lang="less">
@rds-6: 6px;
    .container {
        margin-top: 20px;
        display: flex;
        .sider {
            margin-right: 20px;
            .sider-nav {
                border-radius: @rds-6;
                background-color: #fff;
                .nav-link {
                    padding-left: 20px;
                    padding-right: 20px;
                    border-left: 2px solid #09ffe5;
                    line-height: 2.4em;
                }
            }
        }

        .main {
            flex: 1;
            .bread-wrap {
                padding: 12px 30px;
                border-radius: @rds-6;
                background-color: #fff;
            }

            .require-wrap {
                margin-top: 20px;
                margin-bottom: 40px;
                border-radius: @rds-6;
                background-color: #fff;
                .require-hd {
                    padding: 12px 26px;
                    border-bottom: 1px solid #eee;
                }

                .require-form {
                    padding-top: 10px;
                    padding-left: 30px;
                    .form-control {
                        margin-top: 30px;
                        margin-bottom: 30px;
                        display: flex;
                        align-items: center;
                        flex-wrap: wrap;
                        .ipt {
                            display: inline-block;
                            width:570px;
                            font-size: 16px;
                            padding: .6em 1em;
                            border-radius: 2em;
                            box-shadow: 0 0 1px #c5c5c5;
                            background-color: #f7f8fa;
                        }

                        .placeholder {
                            color: #757575;
                            cursor: pointer;
                        }

                        .select-box {
                            position: absolute;
                            border-radius: @rds-6;
                            box-shadow: 0 0 20px #ccc;
                            background-color: #fff;
                            .type {
                                line-height: 2em;
                                padding-left: 20px;
                                padding-right: 20px;
                                text-align: center;
                                &:hover {
                                    background-color: #eee;
                                }
                            }
                        }

                        .textarea-box {
                            display: inline-block;
                            width:570px;
                            height: 6em;
                            font-size: 16px;
                            padding: .6em 1.4em;
                            border-radius: 6em;
                            box-shadow: 0 0 1px #c5c5c5;
                            background-color: #f7f8fa;
                            textarea {
                                font: inherit;
                                width: 100%;
                                height: 100%;
                                overflow: hidden;
                            }
                        }

                        .file-box {
                           label {
                               display:flex;
                               width: 200px;
                               height: 200px;
                               background-color: #eee;
                               cursor: pointer;
                               &::after {
                                   content: '+';
                                   margin: auto;
                                   display: inline-block;
                                   width: 2em;
                                   height: 2em;
                                   border-radius: 50%;
                                   text-align: center;
                                   font-size: 18px;
                                   line-height: 1.8;
                                   color: #fff;
                                   background-color: #09ffe5;
                               }
                               .ipt-file {
                                   display: none;   
                               }
                           }
                        }
                    }

                    .upload-hd {
                        margin: 40px 20px;
                        padding-top: 10px;
                        border-top: 1px solid #eee;
                        .file-tip {
                            padding-left: 10px;
                            font-size: 14px;
                            color: #f56464;
                        }
                    }

                    .form-control.required::before {
                        content: '*';
                        color: #f56464;
                        padding-right: 20px;
                    }
                        
                }

                .require-ft {
                    padding: 20px 26px;
                    border-top: 1px solid #eee;
                    .btn {
                        margin-right: 20px;
                        display: inline-block;
                        width: 10em;
                        border: none;
                        padding: .6em 2em;
                        border-radius: 2em;
                        color: #fff;
                        background-color: #09ffe5;
                        cursor: pointer;
                    }
                }
            }
        }
    }
</style>

