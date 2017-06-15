# Tree

css:

```
      .slideBox{  width: 400px;  }
      .slide-tree, .slide-tree li,  .slide-tree ul{
          list-style: none;
          margin: 0;
          padding: 0;
      }
      .slide-tree{  font-size: 17px;  margin: 10px 0 10px 0;  }
      .slide-tree ul{  margin-left: 22px;  position: relative;  }
      .slide-tree li{  position: relative;  cursor: pointer;  }
      .slide-tree .slideItem{  padding: 4px  10px;  position: relative;  }
      .slide-tree .slideEditBtn{float: right;cursor: pointer;font-size: 16px}
      .slideName{
          display: block;
          margin-right: 0;
          position: relative;
          cursor: pointer;
      }
      /*有编辑按钮*/
      .slide-tree-edit .slideName{  padding-right: 120px;  }
      .slide-tree-edit .slide-tree-editBox{
          display: inline-block;
          float: right;
          width: 120px;
          position: absolute;
          right: 0;
          top: 0;
          height: 100%;
          line-height: 30px;
          text-align: center;
      }
      .slide-tree-edit .slide-tree-editBox a.slide-tree-btn:last-child{  margin-left: 10px;  }
      .slide-tree-edit .slide-tree-editBox a.slide-tree-checkbox{  position: relative;  top: -2px;  }
      /*竖线*/
      .slide-tree ul li:before{
          content: '';
          position: absolute;
          width: 10px;
          height: 100%;
          border-left: solid 1px #666;
          left: -5px;
          top: -6px;
      }
      /*最后一条LI的竖线固定高度*/
      .slide-tree li ul:last-child >li:before{
          content: '';
          position: absolute;
          width: 10px;
          height: 22px;
          border-left: solid 1px #666;
          left: -5px;
          top: -6px;;
      }
      /*横线*/
      .slide-tree ul li:after{
          content: '';
          width: 13px;
          height: 1px;
          border-top: solid 1px #666;
          position: absolute;
          top: 15px;
          left: -5px;
      }
      
      .icon-folder,
      .icon-open,
      .icon-file{top: 3px}
      /*  有儿子没展开*/
      .icon-folder{
          display: inline-block;
          width: 17px;
          height: 17px;
          border: solid 1px #666;
          position: relative;
          border-radius: 1px;
      }
      .icon-folder:before{
          content: '';
          width: 13px;
          height: 1px;
          background: #666;
          left: 1px;
          top: 7px;
          position: absolute;
      }
      .icon-folder:after{
          content: '';
          width: 1px;
          height: 13px;
          background: #666;
          left: 7px;
          top: 1px;
          position: absolute;
      }
      /*有儿子并展开*/
      .icon-open{
          display: inline-block;
          width: 17px;
          height: 17px;
          border: solid 1px #3ed69e;
          position: relative;
          border-radius: 1px;
      }
      .icon-open:after{
          content: '';
          width: 13px;
          height: 1px;
          background: #3ed69e;
          left: 1px;
          top: 7px;
          position: absolute;
      }
      /*没有儿子*/
      .icon-file{
          display: inline-block;
          width: 17px;
          height: 17px;
          border: solid 1px #666;
          position: relative;
          border-radius: 1px;
      }
      .icon-file:before{
          content: '';
          right: 0;
          top: 0;
          width: 7px;
          height: 4px;
          background: #666;
          left: auto;
          position: absolute;
      }
      
      .tree-act{
          color: #3ed69e;
      }
      .tree-act .icon-file{
          display: inline-block;
          width: 17px;
          height: 17px;
          border: solid 1px #3ed69e;
          position: relative;
          border-radius: 1px;
      }
      .tree-act .icon-file:before{
          content: '';
          right: 0;
          top: 0;
          width: 7px;
          height: 4px;
          background: #3ed69e;
          left: auto;
          position: absolute;
      }

```
### 默认布局



div:

```
<div class="slideBox" >
    <ul class="slide-tree">
        <li class="slideModel ">
            <div class="slideItem ">
                <span class="slideName ellipsis primaryColor">
                    <i class=" icon-open"></i>
                    攻坚2017行动
                </span>
            </div>
            <ul class="slide-tree ">
                <li class="slideModel ">
                    <div class="slideItem ">
                        <span class="slideName ellipsis primaryColor">
                            <i class=" icon-open"></i>
                            攻坚2017行动
                        </span>
                    </div>
                    <ul class="slide-tree ">
                        <li class="slideModel ">
                            <div class="slideItem ">
                                <span class="slideName ellipsis primaryColor">
                                    <i class=" icon-file" ></i>
                                    攻坚2017行动
                                </span>
                            </div>
                        </li>
                    </ul>
                    <ul class="slide-tree ">
                        <li class="slideModel ">
                            <div class="slideItem ">
                        <span class="slideName ellipsis primaryColor">
                            <i class=" icon-file" ></i>
                            攻坚2017行动
                        </span>
                            </div>
                        </li>
                    </ul>
                </li>
            </ul>
        </li>
    </ul>
    <ul class="slide-tree ">
        <li class="slideModel ">
            <div class="slideItem ">
                <span class="slideName ellipsis primaryColor">
                    <i class="icon-folder"></i>
                    攻坚2017行动
                </span>
            </div>
        </li>
    </ul>
</div>

```

### 有编辑按钮最外加上类slide-tree-edit

div:

```$xslt

  <div class="slideBox slide-tree-edit" >
      <ul class="slide-tree">
          <li class="slideModel ">
              <div class="slideItem ">
                  <span class="slideName ellipsis primaryColor">
                      <i class=" icon-open"></i>
                      攻坚2017行动
                  </span>
                  <span class="slide-tree-editBox">
                      <a class="slide-tree-btn">编辑</a><a class="slide-tree-btn">删除</a>
                  </span>
              </div>
              <ul class="slide-tree ">
                  <li class="slideModel ">
                      <div class="slideItem ">
                          <span class="slideName ellipsis primaryColor">
                              <i class=" icon-open"></i>
                              攻坚2017行动
                          </span>
                          <span class="slide-tree-editBox">
                              <a class="slide-tree-checkbox"><input type="checkbox"></a>
                          </span>
                      </div>
                      <ul class="slide-tree ">
                          <li class="slideModel ">
                              <div class="slideItem ">
                          <span class="slideName ellipsis primaryColor">
                              <i class=" icon-file" ></i>
                              攻坚2017行动
                          </span>
                              </div>
                          </li>
                      </ul>
                      <ul class="slide-tree ">
                          <li class="slideModel ">
                              <div class="slideItem ">
                          <span class="slideName ellipsis primaryColor">
                              <i class=" icon-file" ></i>
                              攻坚2017行动
                          </span>
                              </div>
                          </li>
                      </ul>
                  </li>
              </ul>
              <ul class="slide-tree ">
                  <li class="slideModel ">
                      <div class="slideItem ">
                          <span class="slideName ellipsis primaryColor">
                              <i class=" icon-file" ></i>
                              攻坚2017行动
                          </span>
                      </div>
                  </li>
              </ul>
          </li>
      </ul>
      <ul class="slide-tree ">
          <li class="slideModel ">
              <div class="slideItem ">
                  <span class="slideName ellipsis primaryColor">
                      <i class="icon-folder"></i>
                      攻坚2017行动
                  </span>
              </div>
          </li>
      </ul>
  </div>
  
```