# mobile_meta
 Meta description of mobile terminal

## meta标签
### 概要
标签提供关于HTML文档的元数据。元数据不会显示在页面上，但是对于机器是可读的。它可用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他 web 服务。
#### 必要属性

| 属性 | 值 | 描述 | 默认值 |
| ---- | ---- | ---- | ---- |
| content | some text | 定义与http-equiv或name属性相关的元信息 | |

#### 可选属性

| 属性 | 值 | 描述 | 默认值 |
| ---- | ---- | ---- | ---- |
| http-equiv | content-type / expire / refresh / set-cookie | 把content属性关联到HTTP头部。 | |
| name | author / description / keywords / generator / revised / others | 把 content 属性关联到一个名称。 | |
| scheme | some text | 定义用于翻译 content 属性值的格式。   | |


### h5 常用meta标签及说明
#### SEO相关
* keywords
```
<meta name="keywords" content="your tags" />
```
>页面关键字,不应超过 874 个字符.

* description
```
<meta name="description"content="150 words" />
```
>页面描述,不超过 150 个字符.

* robots
```
<meta name="robots" content="index,follow" />  //
<!--  
    all：文件将被检索，且页面上的链接可以被查询；
    none：文件将不被检索，且页面上的链接不可以被查询；
    index：文件将被检索；
    follow：页面上的链接可以被查询；
    noindex：文件将不被检索；
    nofollow：页面上的链接不可以被查询。
 -->
```
>搜索引擎索引方式.

* 页面刷新和重定向
```
<meta http-equiv="refresh" content="0;url=" />
```
* author
```
<meta name="author" content="author name" />
```
>定义网页作者.
#### 移动端常用

```
<meta name="viewport" content="width=device-width, initial-scale=1.0,maximum-scale=1.0, user-scalable=no"/>  
<!-- `width=device-width` 会导致 iPhone 5 添加到主屏后以 WebApp 全屏模式打开页面时出现黑边  -->  
```
> 标签表示：强制让文档的宽度与设备的宽度保持1:1，并且文档最大的宽度比例是1.0，且不允许用户点击屏幕放大浏览；尤其要注意的是content里多个属性的设置一定要用分号+空格来隔开，如果不规范将不会起作用。

其中：

* viewport - 能优化移动浏览器的显示。如果不是响应式网站，不要使用initial-scale或者禁用缩放。
* width - viewport的宽度（数值 / device-width）（范围从200 到10,000，默认为980 像素）
* height - viewport的高度（数值 / device-height）（范围从223 到10,000）
* initial-scale - 初始的缩放比例（范围从>0 到10）
* minimum-scale - 允许用户缩放到的最小比例
* maximum-scale - 允许用户缩放到的最大比例
* user-scalable - 用户是否可以手动缩放(no,yes)
* minimal-ui - 可以在页面加载时最小化上下状态栏。（已弃用）

注意，很多人使用initial-scale=1到非响应式网站上，这会让网站以100%宽度渲染，用户需要手动移动页面或者缩放。如果和initial-scale=1同时使用user-scalable=no或maximum-scale=1，则用户将不能放大/缩小网页来看到全部的内容。

* apple-mobile-web-app-capable

```
<meta name="apple-mobile-web-app-capable" content="yes" />
```
> iphone设备中的safari私有meta标签,启用 WebApp 全屏模式 伪装app，离线应用

* apple-mobile-web-app-status-bar-style
```
<meta name="apple-mobile-web-app-status-bar-style"content="black-translucent" />
```
>隐藏状态栏/设置状态栏颜色：只有在开启WebApp全屏模式时才生效。content的值为default | black | black-translucent

* apple-mobile-web-app-title
```
<meta name="apple-mobile-web-app-title"content="标题">
```
>添加到主屏后的标题

* format-detection telephone
```
<meta content="telephone=no"name="format-detection" />
```
>忽略数字自动识别为电话号码

* format-detection email
```
<meta content="email=no"name="format-detection" />
```
>忽略识别邮箱

* apple-mobile-web-app-capable
```
<meta name="apple-mobile-web-app-capable" content="yes" />
```
>删除苹果默认的工具栏和菜单栏 iphone设备中的safari私有meta标签

* apple-mobile-web-app-status-bar-style
```
<meta name="apple-mobile-web-app-status-bar-style" content="black" />
```
>设置苹果工具栏颜色

* renderer
```
<meta name="renderer" content="webkit">
```
>启用360浏览器的极速模式(webkit)

* HandheldFriendly
```
<meta name="HandheldFriendly" content="true">
```
>针对手持设备优化，主要是针对一些老的不识别viewport的浏览器，比如黑莓

* screen-orientation
```
<meta name="screen-orientation" content="portrait">
```
>uc强制竖屏

* full-screen
```
<meta name="full-screen" content="yes">
```
>UC强制全屏

* browsermode
```
<meta name="browsermode" content="application">
```
>UC应用模式

* x5-orientation
```
<meta name="x5-orientation" content="portrait">
```
>QQ强制竖屏

* x5-fullscreen
```
<meta name="x5-fullscreen" content="true">
```
>QQ强制全屏

* x5-page-mode
```
<meta name="x5-page-mode" content="app">
```
>QQ应用模式


# 移动端适配方案 动态rem、vw适配 。。。 
未完，待续。。。
