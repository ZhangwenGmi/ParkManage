<template lang="html">
    <div id="container">
        <ul class="online-tab">
            <li class="active"><i class="pc"></i></li>
            <li><i class="phone"></i></li>
        </ul>
        <div class="online-wrap">
            <div class="online-item u15">
                <div class="u-item online-box mr mb arr-r">
                    <div class="online-box-t">
                        <h3><em>In conversation</em></h3>
                    </div>
                    <div class="online-box-c">
                        <ul class="speaking">
                            <li><i class="online"></i><span>Liu Yina</span></li>
                        </ul>
                    </div>
                </div>
                <div class="u-item online-box mr">
                    <div class="online-box-t">
                        <h3><em>Offline</em></h3>
                    </div>
                    <div class="online-box-c">
                        <ul class="speaking off">
                            <li><i class="offline"></i><span>Li Yaming</span></li>
                            <li><i class="offline"></i><span>Feng Shuo</span></li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="online-item">
                <div class="u-item online-box mr">
                    <div class="online-box-t cur">
                        <h3><i class="point-yellow"></i><em>Liu Yina</em><span>Entering...</span></h3>
                        <p><span>Time:3'22</span><a href="javascript:;">End service</a></p>
                    </div>
                    <div class="online-box-c input-box">
                        <div class="input-t">
                            <ul>
                                <li class="my-reply">
                                    <div class="favicon"><img src="../../assets/images/service/1.png" width="42" height="42" alt="Li Mingliang">
                                        <br>Li Mingliang</div>
                                    <div class="my-word my-right">Hello, welcome to consult the online customer service, customer service number 6100, very glad to serve you.</div>
                                </li>
                                <li>
                                    <div class="favicon"><img src="../../assets/images/service/1.png" width="42" height="42" alt="Liu Yina">
                                        <br>Liu Yina</div>
                                    <div class="my-word my-left">Hello, welcome to consult the online customer service, customer service number 6100, very glad to serve you.</div>
                                </li>
                                <li class="my-reply">
                                    <div class="favicon"><img src="../../assets/images/service/1.png" width="42" height="42" alt="Li Mingliang">
                                        <br>Li Mingliang</div>
                                    <div class="my-word my-right">Hello, welcome to consult the online customer service, customer service number 6100, very glad to serve you.</div>
                                </li>
                            </ul>
                        </div>
                        <div class="input-b">
                            <div class="input-b-t">
                                <div class="fl">
                                    <b class="icon-emotion"></b>
                                    <b class="icon-picture"></b>
                                    <b class="icon-file"></b>
                                </div>
                                <div class="fr">
                                    <a href="javascript:;" class="ctrl" data-id="quick">Recovery</a>
                                    <a href="javascript:;" class="ctrl" data-id="work">Work order</a>
                                </div>
                            </div>
                            <div class="input-b-c">
                                <textarea name="" id="" cols="" rows=""></textarea>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="online-item u25" data-id="quick">
                <div class="u-item online-box mr">
                    <div class="online-box-t">
                        <h3><i class="icon-back"></i><em>Recovery</em></h3>
                        <a href="javascript:;" class="close-item" title="Close">✕</a>
                    </div>
                    <div class="online-box-c">
                        <ul class="inner-tab">
                            <li class="cur">Knowledge base</li>
                            <li>Personal library</li>
                        </ul>
                        <el-tree :data="data" node-key="id" :default-expanded-keys="[1]" :default-checked-keys="[1]" :props="defaultProps"> </el-tree>
                        <ul class="bottom-btn-list">
                            <li><button class="btn btn-default">Send</button></li>
                            <li><button class="btn">Details</button></li>
                            <li><button class="btn">Collection</button></li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="online-item u25" data-id="work">
                <div class="u-item online-box">
                    <div class="online-box-t">
                        <h3><i class="icon-back"></i><em>Work order</em></h3>
                        <a href="javascript:;" class="close-item" title="Close">✕</a>
                    </div>
                    <div class="online-box-c">
                        <ul class="inner-tab">
                            <li class="cur">Work order input</li>
                            <li>History work order</li>
                        </ul>
                        <div class="work-order">
                            <h3>Information</h3>
                            <el-row>
                              <el-col :span="6">Name:</el-col>
                              <el-col :span="16"><input type="text" placeholder=""></el-col>
                            </el-row>
                            <el-row>
                              <el-col :span="6">Mobile:</el-col>
                              <el-col :span="16"><input type="text" placeholder=""></el-col>
                            </el-row>
                            <el-row>
                              <el-col :span="6">Company:</el-col>
                              <el-col :span="16"><input type="text" placeholder=""></el-col>
                            </el-row>
                            <el-row>
                              <el-col :span="6">Role category:</el-col>
                              <el-col :span="16"><select name="" id=""><option value="1">Service personnel</option></select></el-col>
                            </el-row>
                            <el-row>
                              <el-col :span="6">Business category:</el-col>
                              <el-col :span="16"><select name="" id=""><option value="1">Report</option></select></el-col>
                            </el-row>
                            <el-row>
                              <el-col :span="6">Solution state:</el-col>
                              <el-col :span="16"><select name="" id=""><option value="1">Unsolved</option></select></el-col>
                            </el-row>
                            <el-row>
                              <el-col :span="6">Add remarks:</el-col>
                              <el-col :span="16"><textarea name="" id=""></textarea></el-col>
                            </el-row>
                        </div>
                        <ul class="bottom-btn-list">
                            <li><button class="btn btn-success">Save</button></li>
                            <li><button class="btn">Forward</button></li>
                            <li><button class="btn btn-danger">Close</button></li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'view',
    data: () => ({
        data: [{
            id: 1,
            label: 'Report template',
            children: [{
                id: 5,
                label: 'Purchase report'
            }, {
                id: 6,
                label: 'Warehouse report'
            }, {
                id: 7,
                label: 'Supplier report'
            }, {
                id: 8,
                label: 'Contract report'
            }]
        }, {
            id: 2,
            label: 'Q & A',
            children: [{
                id: 9,
                label: ' Question1'
            }, {
                id: 10,
                label: 'Question2'
            }, {
                id: 11,
                label: 'Question3'
            }, {
                id: 12,
                label: 'Question4'
            }]
        }, {
            id: 3,
            label: 'operation flow'
        }, {
            id: 4,
            label: 'Common words'
        }],
        defaultProps: {
          children: 'children',
          label: 'label'
        }
    }),
    mounted: function() {
        this.navSelection();
    },
    methods: {
        navSelection() {
            $('body').on('click', '.online-tab li', function() {
                $(this).addClass('active').siblings().removeClass('active');
            }).on('click', '.inner-tab li', function() {
                $(this).addClass('cur').siblings().removeClass('cur');
            }).on('click', '.ctrl', function() {
                var id = $(this).attr('data-id'),
                    dom = $('.online-item[data-id="'+ id +'"]');
                if (dom.is(':hidden')) {
                    dom.show();
                }
            }).on('click', '.close-item', function() {
                $(this).parents('.online-item').hide();
            });
        }
    }
}
</script>
<style lang="scss" scoped>
.online-tab {
    height: 52px;
    overflow: hidden;
    li {
        text-align: center;
        width: 400px;
        background: #ededed;
        float: left;
        cursor: pointer;
        border-bottom: 2px solid #b7e0f9;
        height: 50px;
        margin-bottom: 10px;
        i {
            display: inline-block;
            width: 21px;
            height: 21px;
            overflow: hidden;
            vertical-align: top;
            margin-top: 15px
        }
        .pc {
            background: url(../../assets/images/service/pc.png) no-repeat 50% 50%;
        }
        .phone {
            background: url(../../assets/images/service/phone.png) no-repeat 50% 50%;
        }
    }
    .active {
        background: #fff;
    }
}

.online-wrap {
    height: calc(100vh - 157px);
    display: flex;
    .online-item {
        flex: 1;
        display: flex;
        flex-direction: column;
    }
    .u15 {
        flex: 0 0 15%;
    }
    .u25 {
        flex: 0 0 25%;
    }
    .u35 {
        flex: 0 0 35%;
    }
    .u-item {
        flex: 1;
    }
}

.mr {
    margin-right: 10px;
}

.mb {
    margin-bottom: 10px;
}

.online-box {
    flex: 1;
    display: flex;
    flex-direction: column;
    border: 1px solid #ccc;
    background: #fff;
    .online-box-t {
        flex: 0 0 49px;
        border-bottom: 1px solid #b7e0f9;
        padding: 0 10px;
        position: relative;
        overflow: hidden;
        h3 {
            margin: 0;
            font-weight: normal;
            font-size: 14px;
            float: left;
            .icon-back {
                width: 20px;
                height: 20px;
                display: inline-block;
                overflow: hidden;
                vertical-align: top;
                margin: 15px 10px 0 0;
                background: url(../../assets/images/service/back.png) no-repeat 50% 50%;
            }
            em {
                font-style: normal;
                line-height: 49px;
                color: #4799d4;
                display: inline-block;
                vertical-align: top;
            }
        }
    }
    .cur {
        overflow: hidden;
        h3 {
            .point-yellow {
                width: 10px;
                height: 10px;
                overflow: hidden;
                background: #f8e71c;
                display: inline-block;
                vertical-align: top;
                margin: 20px 10px 0 0;
                border-radius: 50%;
            }
            em {
                color: #4d4d4d;
            }
            span {
                color: #b3b3b3;
                line-height: 49px;
                vertical-align: top;
                margin-left: 10px;
            }
        }
        p {
            float: right;
            line-height: 49px;
            span {
                color: #b3b3b3;
                vertical-align: top;
                margin-right: 10px;
                display: line-block;
            }
            a {
                display: line-block;
                color: #e17572;
                &:hover {
                    color: #e17572;
                    text-decoration: none;
                }
            }
        }
    }
    .online-box-c {
        flex: 1;
        position: relative;
    }
}

.input-box {
    display: flex;
    flex-direction: column;
    .input-t {
        color: #595959;
        flex: 0 0 70%;
        overflow-y: auto;
        ul {
            margin: 10px;
        }
        li {
            overflow: hidden;
            min-height: 20px;
            div {
                float: left;
            }
            .favicon {
                width: 50px;
                text-align: center;
            }
            .my-word {
                position: relative;
                max-width: 85%;
                background: #f2f2f2;
                line-height: 20px;
                padding: 10px;
                border: 1px solid #ccc;
                margin-left: 12px;
                &:before {
                    display: block;
                    position: absolute;
                    content: '';
                    overflow: hidden;
                    border-right: 1px solid #ccc;
                    border-bottom: 1px solid #ccc;
                    background: #f2f2f2;
                    width: 7px;
                    height: 7px;
                    top: 16px;
                }
            }
            .my-left {
                &:before {
                    transform: rotate(135deg);
                    -ms-transform: rotate(135deg);
                    /* IE 9 */
                    -moz-transform: rotate(135deg);
                    /* Firefox */
                    -webkit-transform: rotate(135deg);
                    /* Safari 和 Chrome */
                    -o-transform: rotate(135deg);
                    left: -4px;
                }
            }
        }
        .my-reply {
            div {
                float: right;
            }
            .my-word {
                margin-right: 12px;
                margin-left: 0;
            }
            .my-right {
                &:before {
                    transform: rotate(-45deg);
                    -ms-transform: rotate(-45deg);
                    /* IE 9 */
                    -moz-transform: rotate(-45deg);
                    /* Firefox */
                    -webkit-transform: rotate(-45deg);
                    /* Safari 和 Chrome */
                    -o-transform: rotate(-45deg);
                    right: -4px;
                }
            }
        }
    }
    .input-b {
        flex: 0 0 30%;
        display: flex;
        flex-direction: column;
        .input-b-t {
            flex: 0 0 50px;
            background: #f0f0f0;
            overflow: hidden;
            b {
                display: inline-block;
                width: 20px;
                height: 20px;
                vertical-align: top;
                margin: 15px;
                cursor: pointer;
            }
            .icon-emotion {
                background: url(../../assets/images/service/emotion.png) no-repeat 50% 50%;
            }
            .icon-picture {
                background: url(../../assets/images/service/picture.png) no-repeat 50% 50%;
            }
            .icon-file {
                background: url(../../assets/images/service/file.png) no-repeat 50% 50%;
            }
            a {
                display: inline-block;
                height: 50px;
                line-height: 50px;
                padding: 0 15px;
                color: #f4b143;
                text-decoration: none;
                &:hover {
                    text-decoration: none;
                }
            }
        }
        .input-b-c {
            flex: 1;
            background: #fff;
            textarea {
                border: 0 none;
                width: 100%;
                height: 100%;
                padding: 5px;
                line-height: 20px;
                color: #595959;
            }
        }
    }
}

.fl {
    float: left;
}

.fr {
    float: right;
}

.speaking {
    margin: 0 10px;
    li {
        min-height: 40px;
        color: #1cbfb0;
        i {
            width: 19px;
            height: 19px;
            display: inline-block;
            overflow: hidden;
            vertical-align: top;
            margin: 11px 10px 0 0;
        }
        span {
            display: inline-block;
            vertical-align: top;
            height: 40px;
            line-height: 40px;
        }
    }
    .online {
        background: url(../../assets/images/service/online.png) no-repeat 50% 50%;
    }
    .offline {
        background: url(../../assets/images/service/offline.png) no-repeat 50% 50%;
    }
}

.off {
    li {
        color: #b3b3b3;
    }
}

.arr-r {
    position: relative;
    &:before {
        display: block;
        position: absolute;
        content: '';
        overflow: hidden;
        border-right: 1px solid #ccc;
        border-bottom: 1px solid #ccc;
        background: #fff;
        width: 7px;
        height: 7px;
        transform: rotate(-45deg);
        -ms-transform: rotate(-45deg);
        /* IE 9 */
        -moz-transform: rotate(-45deg);
        /* Firefox */
        -webkit-transform: rotate(-45deg);
        /* Safari 和 Chrome */
        -o-transform: rotate(-45deg);
        right: -4px;
        top: 50%;
        margin-top: -3px;
    }
}

.inner-tab {
    display: flex;
    height: 45px;
    li {
        flex: 1;
        background: #f5f5f5;
        color: #b6b6b6;
        text-align: center;
        line-height: 45px;
        cursor: pointer;
    }
    .cur {
        background: #b7e0f9;
        color: #505151;
    }
}
.bottom-btn-list {
    margin: 0;
    position: absolute;
    display: flex;
    width: 100%;
    bottom: 0;
    left: 0;
    height: 68px;
    background: #f2f2f2;
    li {
        flex: 1;
        text-align: center;
        height: 32px;
        padding: 17px 0;
    }
    .btn {
        border: 1px solid #4296d2;
        background: #f2f2f2;
        color: #4296d2;
        height: 30px;
        line-height: 30px;
        padding: 0 15px;
        border-radius: 2px;
    }
    .btn-default {
        background: #4296d2;
        color: #fff;
    }
    .btn-success {
        background: #1cbfb0;
        color: #fff;
        border-color: #1cbfb0;
    }
    .btn-danger {
        background: #d84c49;
        color: #fff;
        border-color: #d84c49;
    }
}
.el-tree {
    margin: 0 10px;
    border: 0 none;
    color: #555;
}
.work-order {
    h3 {
        line-height: 30px;
        margin:0 0 10px 0;
        font-size: 14px;
    }
    line-height: 30px;
    color: #555;
    padding: 0px 10px;
    .el-row {
        margin-bottom: 15px;
    }
    .el-col-6 {
        text-align: right;
    }
    input, select, textarea {
        border: 1px solid #ccc;
        height: 28px;
        width: 100%;
    }
    textarea {
        line-height: 24px;
        height: 60px;
    }
}
.close-item {
    position: absolute;
    right: 10px;
    top: 15px;
    width: 20px;
    height: 20px;
    font-size: 14px;
    line-height: 20px;
    display: block;
    text-align: center;
    overflow: hidden;
    color: #999;
    border-radius: 50%;
    &:hover {
        background: #f0f0f0;
    }
}
</style>