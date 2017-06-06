# CSS-Layout



css:

```
.imgTextList{
            margin-bottom: 30px;
        }
        .imgTextList .dt-con{
            display: inline-block;
            width: 50px;
            height: 50px;
            position: relative;
            border-radius: 50%;
            overflow: hidden;
            margin-top: 2px;
        }
        .imgTextList-dt{
            width: 80px;
            float: left;
            text-align: center;
        }
        .imgTextList-dd{
            display: block;
            margin-left: 80px;
        }
        .dd-title{
            font-size: 17px;
            margin-bottom: 7px;
        }
        .dd-con{
            color: #666666;
            font-size: 14px;
            line-height: 18px;
        }
```

div:

```
<div>
    <dl class="imgTextList">
        <dt class="imgTextList-dt">
            <span class="dt-con"><img src="aa1.png" width="100%"></span>
        </dt>
        <dd class="imgTextList-dd">
            <div>
                <div class="dd-title">SOS一键报警</div>
                <div class="dd-con">点击“SOS”，进入视频警告、现场拍照界面；视频警告阻吓犯罪的发生。</div>
            </div>
        </dd>
    </dl>
    <dl class="imgTextList">
        <dt class="imgTextList-dt">
            <span class="dt-con"><img src="aa2.png" width="100%"></span>
        </dt>
        <dd class="imgTextList-dd">
            <div>
                <div class="dd-title">静默报警</div>
                <div class="dd-con">静默方式下报警求救，无视频警告；无声无息对犯罪现场以及犯罪分子的信息进行采集上传至服务器。</div>
            </div>
        </dd>
    </dl>
    <dl class="imgTextList">
        <dt class="imgTextList-dt">
            <span class="dt-con"><img src="aa3.png" width="100%"></span>
        </dt>
        <dd class="imgTextList-dd">
            <div>
                <div class="dd-title">出行守护</div>
                <div class="dd-con">选择“出行守护”，分享您的行程轨迹；让您的守护人可以随时看到您的行程动态。</div>
            </div>
        </dd>
    </dl>
    <dl class="imgTextList">
        <dt class="imgTextList-dt">
            <span class="dt-con"><img src="aa.png" width="100%"></span>
        </dt>
        <dd class="imgTextList-dd">
            <div>
                <div class="dd-title">周边事件</div>
                <div class="dd-con">受害者遇到危险，平台将求救事件推送到周边用户，附近用户可以到现场进行拍摄取证，进一步报警或者解救受害者。</div>
            </div>
        </dd>
    </dl>
    <dl class="imgTextList">
        <dt class="imgTextList-dt">
            <span class="dt-con"><img src="aa.png" width="100%"></span>
        </dt>
        <dd class="imgTextList-dd">
            <div>
                <div class="dd-title">消息推送</div>
                <div class="dd-con">系统可以进行求救事件、好友请求、公告等信息的推送；方便您能及时获取相关消息。</div>
            </div>
        </dd>
    </dl>
</div>
```