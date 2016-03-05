### 伪类元素（ before after）
伪元素”，顾名思义。它创建了一个虚假的元素，并插入到目标元素内容之前或之后。
像幽灵一般的元素插入在css中，他们对用户是可见的，可以通过css控制。

#### 基本语法
```
	#example:before {
	  content: "#";
	}
	 
	#example:after {
	  content: ".";
	}
```

1. 我们用#example:before和#example:after来目标锁定相同的元素
1. 伪元素如果没有设置“content”属性，伪元素是无用的,所以content属性是必须的

>你可以设置content属性值为空，并且仅仅把他当做一个内容很少的盒子。像这样:
```
	#example:before {
	  content: "";
	  display: block;
	  width: 100px;
	  height: 100px;
	}
```
> 你不可以完全的移除content属性，如果你移除了，伪元素将不会起作用。至少，content属性需要空引用作为它的值(即:content:“”)

### 插入伪类元素的特点
1. 插入元素在页面的内容里是不可见的，只有在css代码中见到。
1. 插入元素在默认情况下是内联元素，因此为了给插入的元素赋予高度，填充，等一系列值的时候需要手动设置成display：block 的块级元素。




















