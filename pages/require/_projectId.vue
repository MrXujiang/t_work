<template>
    <div class="require-detail w">
        <div class="main">
            <div class="require-hd">
                <div class="require-tit">汇桔平台设计</div>
                <div class="publish-time">3小时前<span class="rest-time">离结束还有5天</span></div>
                <div class="require-info">
                    <div class="require-loaction">
                        <div class="locate">地点：武汉科技大学图书馆</div>
                        <div class="reward">奖金：5000元</div>
                    </div>
                    <div class="require-view">
                        <div class="view-num">浏览量(222)</div>
                        <div class="flover">赞(33)</div>
                    </div>
                </div>
            </div>
            <div class="content">
                <div>我们要做一个小程序，小啊小程序。</div>
                <div class="require-ft">
                    <button class="btn do-btn">接单</button>
                    <button class="btn flover-btn">赞</button>
                </div>
            </div>
        </div>
        <div class="sider">
            <div class="user-wrap">
                <div class="tx"><img src="~/assets/images/joiner.png" alt=""></div>
                <div class="nick">猪先森的猪</div>
                <div class="user-info">武汉 | 学生</div>
                <div class="opera-area">
                    <button class="btn follow-btn">关注</button>
                    <button class="btn mes-btn">私信</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped lang="less">
    .require-detail {
        margin-top: 20px;
        display: flex;
        min-height: 100vh;
        .main {
            flex: 1;
            .require-hd {
                padding: 20px;
                border-radius: 6px;
                background-color: #fff;
                .require-tit {
                    font-size: 24px;
                    line-height: 2em;
                }
                .publish-time {
                    font-size: 14px;
                    color: #999;
                    line-height: 2em;
                    .rest-time {
                        padding-left: 10px;
                        color: #f56464
                    }
                }

                .require-info {
                    margin-top: 10px;
                    display: flex;
                    font-size: 14px;
                    color: #999;
                    .require-loaction {
                        flex: 1;
                        display: flex;
                        align-items: flex-end;
                        .reward {
                            padding-left: 40px;
                            font-size: 20px;
                            color: #f56464;
                        }
                    }

                    .require-view {
                        display: flex;
                        .view-num {
                            margin-right: 30px;
                        }
                    }
                }
            }

            .content {
                margin-top: 20px;
                padding: 20px;
                border-radius: 6px;
                background-color: #fff;
                .require-ft {
                    margin-top: 30px;
                    padding-top: 20px;
                    border-top: 1px solid #eee;
                    text-align: center;
                    .btn {
                        width: 160px;
                        border-radius: 3em;
                        line-height: 3em;
                        font-size: 16px;
                        color: #fff;
                        background-color: #ececec;
                        cursor: pointer;
                    }

                    .do-btn {
                        background-color: #26C2A0;
                    }

                    .flover-btn {
                        margin-left: 30px;
                        background-color: #f56464;
                    }
                }
            }
        }

        .sider {
            margin-left: 20px;
            .user-wrap {
                padding: 20px;
                width: 260px;
                border-radius: 6px;
                text-align: center;
                background-color: #fff;
                .tx {
                    display: inline-block;
                    width: 100px;
                    height: 100px;
                    border-radius: 50%;
                    overflow: hidden;
                    img {
                        width: 100%;
                    }
                }

                .nick {
                    margin-top: 20px;
                    margin-bottom: 20px;
                    font-weight: bold;
                }

                .user-info {
                    font-size: 14px;
                    color: #ccc;
                }

                .opera-area {
                    margin-top: 20px;
                    .btn {
                        width: 80px;
                        border-radius: 2.2em;
                        line-height: 2.2em;
                        font-size: 16px;
                        color: #fff;
                        background-color: #ececec;
                        cursor: pointer;
                    }

                    .follow-btn {
                        margin-right: 10px;
                        background-color: #f56464;
                    }

                    .mes-btn {
                        background-color: #26C2A0;
                    }
                }
            }
        }
    }
</style>

