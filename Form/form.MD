# CSS-Layout

css:

```css
/*我的表单*/
 .formOutBox{  position: relative;  }
        .formBtnBox{
            width: 150px;
            float: right;
            position: absolute;
            right: 0;
            height: 100%;
            top: 0;
            z-index: 2;
        }
        .formBtnBox .btn{
            position: absolute;
            top: 50%;
            margin-top: -15px;
            right: 30px;
        }
        .formBox{  margin-right: 150px;  color: #69717d;  }
        .formBoxUnit{  width: 25%;  float: left;  }
        .formBoxUnit .inputLabel{
            text-align: right;
            width: 100px;
            float: left;
            padding-top: 11px;
        }
        .formOutBox .inputBox{  margin-left: 105px;  padding: 7px;  }
        .formOutBox .inputStyle{padding: 0 4px}
        .formOutBox .inputBox .inputStyle{
            border-radius: 3px;
            width: 100%;
            resize: none;
            border: solid 1px #ced7e5;
        }
        .formOutBox .inputBox input[type=text].inputStyle,
        .formOutBox .inputBox select.inputStyle{
            min-height: 30px;
        }
        .formOutBox .inputBox textarea.inputStyle{
            min-height: 60px;
        }
        /*用于checkBox和radio*/
        .formOutBox .checkboxRadio{  display: inline-block;  height: 30px;  line-height: 30px;  }
        .formOutBox  .checkboxRadioStyle{
            position: relative;
            top: 1px;

            margin-right: 20px;
        }
        /*有背景色的表单*/
        .bgForm{  background: #eee;  border-top: solid 1px #e6e6e6;  }
        .bgForm .formBox {margin-right:0}
        .bgForm .formBoxUnit{
            border-bottom: solid 1px #e6e6e6;
            padding: 0 1px;
            width: 100%;
            float: none;
        }
        .bgForm .inputBox{  background: #fff;  }

```
### 内联表单

![内联表单](https://github.com/an55555/CSS-Layout/blob/master/Form/form-inline.png?raw=true)


div:

```html
<div class="formOutBox">
    <div class="formBtnBox">
        <span class="btn btn-big btn-primary">查询</span>
    </div>
    <div class="formBox">
        <div>
            <div class="formBoxUnit">
                <label class="inputLabel">
                    事件类型：
                </label>
                <div class="inputBox">
                    <select class="inputStyle">
                        <option>请选择</option>
                        <option>交通事故</option>
                        <option>刑事案件</option>
                    </select>
                </div>
            </div>
            <div class="formBoxUnit">
                <label class="inputLabel">
                    求救人：
                </label>
                <div class="inputBox">
                    <input type="text" class="inputStyle">
                </div>
            </div>

            <div class="formBoxUnit">
                <label class="inputLabel">
                    手机号码：
                </label>
                <div class="inputBox">
                    <input type="text" class="inputStyle">
                </div>
            </div>
            <div class="formBoxUnit">
                <label class="inputLabel">
                    发生时间：
                </label>
                <div class="inputBox">
                    <input type="text" class="inputStyle" onclick="WdatePicker()" placeholder="请选择时间">
                </div>
            </div>
        </div>
        <div>
            <div class="formBoxUnit">
                <label class="inputLabel">
                    状态：
                </label>
                <div class="inputBox">
                    <select class="inputStyle">
                        <option>请选择</option>
                        <option>求救中</option>
                        <option>已解除</option>
                    </select>
                </div>
            </div>
            <div class="formBoxUnit">
                <label class="inputLabel">
                    地点：
                </label>
                <div class="inputBox">
                    <input type="text" class="inputStyle">
                </div>
            </div>
            <div class="formBoxUnit">
                <label class="inputLabel">
                    复选框：
                </label>
                <div class="inputBox">
                    <span class="checkboxRadio">
                        <label>男：</label>
                        <input type="checkbox" class="checkboxRadioStyle">
                    </span>
                    <span class="checkboxRadio">
                        <label>男：</label>
                        <input type="checkbox" class="checkboxRadioStyle">
                    </span>
                    <span class="checkboxRadio">
                        <label>男：</label>
                        <input type="radio" class="checkboxRadioStyle">
                    </span>
                    <span class="checkboxRadio">
                        <label>男：</label>
                        <input type="radio" class="checkboxRadioStyle">
                    </span>
                </div>
            </div>
        </div>

    </div>
</div>
```

### 块级表单-最后层加上类bgForm

![Block-form demo](https://github.com/an55555/CSS-Layout/blob/master/Form/form-block.png?raw=true)

div:

```html
    <div class="formOutBox bgForm">
        <div class="formBox">
            <div>
                <div class="formBoxUnit">
                    <label class="inputLabel">
                        事件类型：
                    </label>
                    <div class="inputBox">
                        <select class="inputStyle">
                            <option>请选择</option>
                            <option>交通事故</option>
                            <option>刑事案件</option>
                        </select>
                    </div>
                </div>
                <div class="formBoxUnit">
                    <label class="inputLabel">
                        求救人：
                    </label>
                    <div class="inputBox">
                        <input type="text" class="inputStyle">
                    </div>
                </div>
    
                <div class="formBoxUnit">
                    <label class="inputLabel">
                        手机号码：
                    </label>
                    <div class="inputBox">
                        <input type="text" class="inputStyle">
                    </div>
                </div>
                <div class="formBoxUnit">
                    <label class="inputLabel">
                        发生时间：
                    </label>
                    <div class="inputBox">
                        <input type="text" class="inputStyle" onclick="WdatePicker()" placeholder="请选择时间">
                    </div>
                </div>
            </div>
            <div>
                <div class="formBoxUnit">
                    <label class="inputLabel">
                        状态：
                    </label>
                    <div class="inputBox">
                        <select class="inputStyle">
                            <option>请选择</option>
                            <option>求救中</option>
                            <option>已解除</option>
                        </select>
                    </div>
                </div>
                <div class="formBoxUnit">
                    <label class="inputLabel">
                        地点：
                    </label>
                    <div class="inputBox">
                        <input type="text" class="inputStyle">
                    </div>
                </div>
                <div class="formBoxUnit">
                    <label class="inputLabel">
                        复选框：
                    </label>
                    <div class="inputBox">
                        <span class="checkboxRadio">
                            <label>男：</label>
                            <input type="checkbox" class="checkboxRadioStyle">
                        </span>
                        <span class="checkboxRadio">
                            <label>男：</label>
                            <input type="checkbox" class="checkboxRadioStyle">
                        </span>
                        <span class="checkboxRadio">
                            <label>男：</label>
                            <input type="radio" class="checkboxRadioStyle">
                        </span>
                        <span class="checkboxRadio">
                            <label>男：</label>
                            <input type="radio" class="checkboxRadioStyle">
                        </span>
                    </div>
                </div>
            </div>
    
        </div>
    </div>
```
