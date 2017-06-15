# CSS-Layout

![DEMO](https://github.com/an55555/CSS-Layout/blob/master/List/imgText.png?raw=true)

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
```
