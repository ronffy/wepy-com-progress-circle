
# 微信小程序wepy的第三方组件：圆形进度条

![](http://oxk008h6r.bkt.clouddn.com/demo.png)

## 说明

官方支持的进度条只有条形进度条，没有圆形进度条，因此增加了一个圆形进度条。
此组件是wepy的第三方组件，因为需要依赖[wepyjs](https://github.com/Tencent/wepy)

## 使用

### 安装组件

```shell
npm install wepy-com-progress-circle --save
```

### 使用组件

```javascript
// index.wpy
<template>
    <progressCircle :percent="percent" width="120" />
</template>
<script>
    import wepy from 'wepy';
    import ProgressCircle from 'wepy-com-progress-circle';

    export default class Index extends wepy.page {
        components = {
            progresscircle: ProgressCircle
        };
        data = {
          percent: 25, 
        }
    }
</script>
```

## API说明

属性名             类型          默认值        说明
percent           Float        0            百分比0~100
width             Number       100          圆的宽度
showInfo	        Boolean	     true	        在进度条右侧显示百分比
strokeWidth	      Number	     6	          进度条线的宽度，单位px
color	            Color        #09BB07	    进度条颜色
backgroundColor	  Color		     #eee         进度条背色颜色

