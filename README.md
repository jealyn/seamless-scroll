# seamless-scroll

纯CSS实现无缝滚动(多图无限轮播)效果

## 何为无缝滚动？

在某些场景下，需要在页面中循环滚动地展示一些信息，如商品信息、营销活动图片、系统消息通知等。

在网页中，滚动是指元素在某个方向的位移过程；无缝，指的是元素上一次滚动结束和下一次滚动开始之间是平滑自然、紧密相连的，如同圆环一样首尾相接、不分起点与终点。

以横向滚动的图片为例，其无缝滚动示意图如下所示：

![无缝滚动示意图](https://mmbiz.qpic.cn/mmbiz_gif/wnFvhQqHtzy0HhTkvXTmxVKc70O7o6ywfpJAMHJjLFwXn0uw3nPChd5nUHOJ0v26IqVDZ0UYMGAXgLOcdYNUNw/0?wx_fmt=gif)


## 实现方式

这里采用近乎纯CSS的方式实现，使用 `animation`和`transform`来实现，以开启 GPU 加速，提升动画流畅度。

### animation

`animation`属性说明如下所示：

| 属性值 | 说明 | 可选值 | 初始值 |
| --- | --- | --- | --- |
| animation-name | 指定动画的名称 | --- | none |
| animation-duration | 指定动画周期的时长 | \<time\> | 0s |
| animation-timing-function | 定义动画的运行效果 | \<timingfunction\> | ease |
| animation-delay | 定义动画于何时开始 | \<time\> | 0s |
| animation-iteration-count | 定义动画运行次数 | infinite \| \<number\> | 1 |
| animation-direction | 指示动画播放方向 | normal \| alternate \| reverse \| alternate-reverse | normal |
| animation-fill-mode | 设置动画在执行前和执行后如何将样式应用于其目标 | none \| forwards \| backwards \| both | none |
| animation-play-state | 定义动画是运行或者暂停 | running \| paused | running |


### transform

`transform`(部分)属性说明如下所示：

| 属性值 | 说明 |
| --- | --- |
| none | 不应用任何变换 |
| matrix(a, b, c, d, tx, ty) | 指定2d变换矩阵 | 
| matrix3d(a1, b1, c1, d1, a2, b2, c2, d2, a3, b3, c3, d3, a4, b4, c4, d4) | 指定3d变换矩阵 | 
| perspective(\<length\>) | 定义z=0平面与用户之间的距离，以便实现透视效果 | 
| rotate3d(x, y, z, a\<angle\>) | 按指定角度旋转元素 | 
| scale3d(sx, sy, sz) | 缩放元素 | 
| skew(ax, ay) | 拉伸、斜切元素 | 
| translate3d(tx, ty, tz) | 移动元素 |