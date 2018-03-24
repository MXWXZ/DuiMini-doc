# UIText
文本  
xml名：txt  
基类：[UIControl](UIControl.md)

|属性|合法值|默认值|说明|
| :---: | :---: | :---: | :---: |
|**background**|**1/0**|**1**|**Text控件默认属于窗口背景**|
|text|字符串||显示文本|
|font|uires字体名|uires默认设置|配置文件中定义的字体|
|fontname|系统字体名|uires默认设置|真实使用的字体名|
|fontsize|正整数|uires默认设置|文本大小|
|fontbold|0/1|uires默认设置|是否加粗|
|fontitalic|0/1|uires默认设置|是否斜体|
|fontunderline|0/1|uires默认设置|是否下划线|
|fontstrikeout|0/1|uires默认设置|是否删除线|
|color|颜色|#FF000000|字符颜色|
|trimming|见表|none|去尾模式|
|autowrap|1/0|0|是否自动换行|
|vertical|1/0|0|是否垂直输出|
|align|见表|lt|对齐方式|

注：去尾模式见下表
|模式名|值|
| :---: | :---: |
|无|none|
|按字符|ch|
|按单词|word|
|按字符加省略号|dotch|
|按单词加省略号|dotword|
|中间加省略号|dotmid|

对齐方式见下表
|模式名|值|
| :---: | :---: |
|lt|左上|
|mt|中上|
|rt|右上|
|lm|左中|
|mm|居中|
|rm|右中|
|lb|左下|
|mb|中下|
|rb|右下|

注：指定`font`属性，将会用`uires`配置文件中的设置初始化**所有属性**，也可指定以`font`开头的属性单独设置字体样式，最后设置的属性优先级最高。
注：`alpha`属性将会转换为百分比和`color`中的透明度相乘。

* * * * *

|函数名|说明|
| :---: | :---: |
|SetFont|设置字体|
|GetText|获取文本|
|SetText|设置文本|
|SetColor|设置颜色|
|GetColor|获取颜色|
|SetTrimming|设置去尾模式|
|GetTrimming|取得去尾模式
|AutoWrap|多行显示|
|Vertical|垂直显示|
|SetAlign|设置对齐方式|
|GetAlign|取得对齐方式|