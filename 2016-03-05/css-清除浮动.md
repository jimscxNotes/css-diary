### 清除浮动
1. 使用div空标签清除浮动（如果不是块级元素，设置display：block）
    ```
    .clear{clear:both}
    <div class=”clearfix″>
        <div class=”left”>我是左浮动</div>
        <div class=”right”>我是右浮动</div>
        <div class=”clear”></div>
    </div>
    ```
1. 父元素设置 overflow：hidden；
1. 父级div定义 伪类:after 和 zoom
    ```
    .clearfix:after {content:”\200B”; display:block; height:0; clear:both; }
    .clearfix { *zoom:1; } 照顾IE6，IE7就可以了
    ```