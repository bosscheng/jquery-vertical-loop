#  垂直滚动文字组件，支持倒叙，正序，适合今日头条类型。


## 概述

特点如下：
1. 支持ES6, CMD, AMD 写法。
2. 支持jquery plugin 插件调用方式。

## html DOM 推荐结构

```
<div class="demo1" >
    <ul>
        <li> </li>
        <li> </li>
    </ul>
</div>
```

### 注意项目

1. 要求 `外层div` 高度必须设置，`内层li` 高度必须设置。
2. 要求 `内层li` 个数必须是是可以被整除的。不然会出现异常。
3. `外层div` 的高度必须是 `内层li` 高度的整数倍。不然会存在滚动出现不全的数据。
4. 由于滚动的css动画是1s内完成的，所以要求`切换(delay)`的时间必须大于1s，不然会出现异常滚动。

## api

### ES6

```
impoort VerticalLoop from "web-vertical-loop";

let verticalLoop = new VerticalLoop({

})
```


### jquery plugin


``` js
$('.demo2').verticalLoop({

});
```

### 参数

|名称	|类型	|默认值	|描述
|:------|:------|:------|:------
|delay	|number	| 5000	| 垂直轮播文字切换间隔时间 单位 ms
|order	|string	| asc	| 轮放滚动的方向 默认 asc （正序）， desc (倒序)
|oninitend	|function	| null	| slide 初始化结束响应函数，返回值： $container 对象


### demo
