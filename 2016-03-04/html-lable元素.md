
## lable
有些浏览器在<form></form>标签之中，你会发现，没有任何标签之间如果写了文字，会使该表单的显示出错，这时，便引入了这个label标签。

### Label标识有两个属性，一个是for，一个是 accesskey。

#### for属性：
        * 功能：表示这个Lable是为哪个控件服务的，Label标签要绑定了FOR指定HTML元素的ID或name属性，你点击这个标签的时候，所绑定的元素将获取焦点。
        * 用法：<label for="InputBox">姓名</label><input id="InputBox" type="text">
#### accesskey属性：
        * 功能：定义了访问这个控件的热键。
        * 用法：<label for="InputBox" accesskey＝"N">姓名</label><input id="InputBox" type="text">
        * 局限性：accessKey属性所设置的快捷键不能与浏览器的快捷键冲突，否则将优先激活浏览器的快捷键。
>关于lable元素的用处：可以使用改变元素的样式例子

```
<div class="select-item">
        <span class="select-item-tt">性别</span>
        <label for="radio-male" style="top:0;left: 58px">
            <input type="radio" name="sex" id="radio-male" value="男"/>
            <i class="rl-icon rl-icon-contact-filled"></i>
            <span>男</span>
        </label>
        <label for="radio-female" style="top:0;left:145px">
            <input type="radio" name="sex" id="radio-female" value="女"/>
            <i class="rl-icon rl-icon-person-filled"></i>
            <span>女</span>
        </label>
</div>

.select-item{
    padding-left: 15px;
    background-color: #fff;
    height: 53px;
    line-height: 53px;
    position: relative;
    font-size: 18px;
    border-bottom: 1px solid #f2f2f2;
}
.select-item label{
    display: block;
    position: absolute;
    height: 53px;
}
自动对焦功能是lable常用的；可以把radio，checkbox，隐藏掉，然后使用字体图标就可以和完美的解决样式啦~~~~~~

```
