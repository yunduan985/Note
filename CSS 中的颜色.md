@[TOC](CSS 中的颜色)

# CSS中颜色的一些表示方法

十六进制色
RGB 颜色
RGBA 颜色
HSL 颜色
HSLA 颜色

## 所有浏览器度支持RGB颜色值

RGB分别是red、green、blue三种颜色的缩写，它们也是三原色，理论上可以调配成任意颜色。

rgb(red, green, blue)。每个参数 (red、green 以及 blue) 定义颜色的强度，可以是介于 0 与 255 之间的整数，或者是百分比值（从 0% 到 100%）。



举例说，rgb(0,0,255) 值显示为蓝色，这是因为 blue 参数被设置为最高值（255），而其他被设置为 0。

同样地，下面的值定义了相同的颜色：rgb(0,0,255) 和 rgb(0%,0%,100%)。


## RGBA
RGBA颜色值得到以下浏览器的支持：IE9+、Firefox 3+、Chrome、Safari 以及 Opera 10+。

RGBA 颜色值是 RGB 颜色值的扩展，它多带了一个透明度的属性。 A是alpha 的缩写。
RGBA 颜色值是这样规定的：rgba(red, green, blue, alpha)。alpha 参数是介于 0.0（完全透明）与 1.0（完全不透明）的数字。
### HSL 颜色
HSL 颜色值得到以下浏览器的支持：IE9+、Firefox、Chrome、Safari 以及 Opera 10+。

HSL 发布时 hue（色调）、saturation（饱和度）、lightness（亮度） 的缩写- 表示颜色柱面坐标表示法。

HSL 颜色值是这样规定的：hsl(hue, saturation, lightness)。

Hue 是色盘上的度数（从 0 到 360） - 0 (或 360) 是红色，120 是绿色，240 是蓝色。Saturation 是百分比值；0% 意味着灰色，而 100% 是全彩。Lightness 同样是百分比值；0% 是黑色，100% 是白色。

#### HSLA 颜色
HSLA 颜色值得到以下浏览器的支持：IE9+、Firefox 3+、Chrome、Safari 以及 Opera 10+。

HSLA 颜色值是 HSL 颜色值的扩展，带有一个 alpha 通道 - 它规定了对象的不透明度。

HSLA 颜色值是这样规定的：hsla(hue, saturation, lightness, alpha)，其中的 alpha 参数定义不透明度。alpha 参数是介于 0.0（完全透明）与 1.0（完全不透明）的数字。
### 十六进制表示法
以#字符开始，#FF00AA，每两位符号分别代表该颜色红绿蓝各自的权重。FF表示16进制取值最大的255，表示红色的比例为100%，00表示16进制的最小值0，16进制表示的数字0~15分别用0 ,1，2, 3，4, 5，6, 7，8 , 9，A, B，C，D，E，F 符号来表示。
