# CSS-Layout

![table demo](https://github.com/an55555/CSS-Layout/blob/master/Table/table.png?raw=true)

css:

```css
  .tableStyle {
            width: 100%;
            background: #fff;
            border-collapse:collapse;  /*重叠的border合度为一条线*/
            /*控制cellpadding-单元格间距-单元边沿与单元内容之间的空间*/
            margin: 0;
            padding: 0;
        }
        .tableStyle td, .tableStyle th {
            text-align: left;
            border: solid 1px #cccccc;
            padding:0; /*控制cellpadding-单元格间距*/
        }
        .tableStyle th {  background: #f3f3f3;  }
        .tableStyle th .th-p{
            color: #666;
            font-weight: bold;
            word-break: keep-all;   /*th里的内容强制不换行，即最小宽度为字段宽度*/
        }

        .tableStyle td.firstTd {
            width: 50px;
            text-align: center;
        }
        .tableStyle td {
            white-space: normal;
            word-break: break-all;
            /*background-clip: padding-box;*/
        }
        .tableStyle .td-p,
        .tableStyle .th-p{
            padding: 10px;
            margin: 0;
        }
        .tableStyle tr:nth-child(even){  background: #fafafa;  }
        .tableStyle .tableCheckBox{position: relative;top: 1px}
         /*保持单行，超出显示省略号*/
        .tableEllipsis{table-layout: fixed}

        .tableEllipsis .td-p,
        .tableEllipsis .th-p{
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        /*.tableStyle tr:hover{  background: #f5f5f5}*/
```

div:

```html
<div class="tableOutBox">
    <table  class="tableStyle tableStyleKeepAll" >
        <thead>
        <tr>
            <th class="firstTd"><p class="th-p">序号</p></th><th><p class="th-p">用户名</p></th> <th><p class="th-p">管理员</p></th> <th><p class="th-p">角色</p></th> <th><p class="th-p">分组</p></th> <th><p class="th-p">操作</p></th>
        </tr>
    </thead>
        <tbody>
        <tr>
      <td class="firstTd"><p class="td-p"><span class="tableCheckBox"><input type="checkbox"></span>1</p></td>
            <td><p class="td-p">小组1-1</p></td>
            <td><p class="td-p">否</p></td>
            <td><p class="td-p">录入员（组员）</p></td>
            <td><p class="td-p">小组1</p></td>
            <td class="operateTd"><p class="td-p"><span class="edit">编辑</span><span class="delete">删除</span></p></td>
        </tr>
        <tr>
            <td class="firstTd"><p class="td-p"><span class="tableCheckBox"><input type="checkbox"></span>1</p></td>
            <td><p class="td-p">小组1-1</p></td>
            <td><p class="td-p">否</p></td>
            <td colspan="2"><p class="td-p">合并单元格</p></td>
            <td class="operateTd"><p class="td-p"><span class="edit">编辑</span><span class="delete">删除</span></p></td>
        </tr>
    </tbody>
    </table>
</div>
```
