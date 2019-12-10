#块元素 block element(dispaly:block;)
1.独占一行，总是在新行上开始
2.宽度缺省的话继承父元素的宽高，可以通过width和heights属性自行设定
3.高度行高、内外边距都可以设置
4.可以容纳其他内联元素
## 常见的块元素
* address - 地址
* blockquote - 块引用
* center - 居中对齐
* dir - 目录列表
* div - 常见的块级容器，是CSS layout的主要标签
* dl - 自定列表
* fieldset - form 控制组
* form - 交互表单
* h1-h6 - 各级标题
* hr - 水平分隔线 
* isindex - input prompt 
* menu - 菜单列表
* noframes - frames 可选内容（对于不支持frame的浏览器显示此块内容）、
* ol - 有序列表
* p - 段落
* pre - 格式化文本
* table - 表格
* ul - 无序列表
# 行内元素inline element (dispaly:inline;)
## 行内元素的特性
1. 和其他元素都在一行上，遇到父级元素边界会自动换行
2. 宽高由内容决定
3. 行内元素只能容纳文本或者其他行内元素 
4. 对于行内元素，需要注意的是：设置宽度width和height都无效，可以设置line-height来设置，margin和padding只有左右有效，上下无效

## 常见的行内元素
* a - 锚点
* abbr - 缩写
* acronym - 首字
* b - 粗体
* bdo - bidi override
* big - 大字体
* br - 换行
* cite - 引用
* code - 计算机代码(在引用源代码的时候需要)
* dfn - 定义字段
* em - 强调
* font - 字体
* i - 斜体
* img - 图片
* input - 输入框
* kbd - 定义键盘文本
* label - 表格标签
* q - 短引用
* s - 中下划线
* samp - 定义范例计算机代码
* select - 项目选择
* small - 小字体文本
* span - 常用内联容器，定义文本区内块
* strick - 中划线
* strong - 粗体强调
* sub - 下标
* sup - 上标
* textarea - 多行文本输入框
* tt - 电传文本
* u - 下划线
* var - 定义变量
## 行内元素的间距问题
* 两个行内元素在一起，会出现一定的间距，即使将border、padding、margin都设置为0，也是没有效果，解决方法如下：

将行内元素的直接父级元素设置font-size = 0px;再给行内元素设置字体大小就可以解决。
2. 方法二：借助html注释
在两个行内元素之间加入HTML注释，告诉这个浏览器这之间既不是换行也不是空格，而是连接在一起的，这样也可以解决
## 可变元素
可变元素为根据上下文语境决定该元素为行内块元素或者内联元素。
* applet - java applet
* button - 按钮
* del - 删除文本
* iframe - inline frame
* ins - 插入的文本
* map - 图片区块(map)
* object - object对象
* script - 脚本客户端
# 行内块元素 inline-block(display:inline-block;)
## 行内元素的特性
1. 元素排列在一行
2. 宽度默认由内容决定
3. 元素之间默认会有间距
4. 支持宽高、外边距、内边距的所有样式的设置
# CSS 设计bug
## margin塌陷
父元素没有顶部了对于margin熟悉来说，所以子元素设置margin不起作用。
父子嵌套的垂直margin熟悉是绑定在一起的，就是margin-top或者margin-bottom。
也就是说子元素的margin-top相对于父元素不起作用，只有当子元素的margin-top
超过父元素设置的话，那么他将整体带动父元素变成margin-top的值

