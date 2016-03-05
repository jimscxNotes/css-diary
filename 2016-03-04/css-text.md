## text 专题
### text-align 属性规定文字的对齐方式
* left      行内内容向左侧边对齐。
* right     行内内容向右侧边对齐。
* center    行内内容居中。
* <string>  第一个出现的该（单字符）字符串被用来对齐。跟随的关键字定义对齐的方向。例如，可用于让数字值根据小数点对齐。
* justify   文字向两侧对齐。


###text-overflow; 属性规定当文本溢出包含元素时发生的事情
* clip	 	修剪文本。
* ellipsis 	显示省略符号来代表被修剪的文本。
* string	使用给定的字符串来代表被修剪的文本。

###text-indent; 属性规定文本块中首行文本的缩进。
>注释：允许使用负值。如果使用负值，那么首行会被缩进到左边。

* length	定义固定的缩进。默认值：0。
* %	        定义基于父元素宽度的百分比的缩进。
* inherit	规定应该从父元素继承 text-indent 属性的值。

###text-transform 
* Capitalize 英文拼音的首字母大写
* Uppercase  英文拼音字母全大写
* Lowercase  英文拼音字母全小写

### 给body设置样式,让页面酷炫
```
body {
    font-family: "微软雅黑";
    background: url(../img/bg.jpg) no-repeat center bottom;
    color: #FFFFFF;
    background-size: 100%;
}
```
### [实现双下滑虚线](index.html)

