# UIControl
所有控件的基类

|属性|合法值|默认值|说明|
| :---: | :---: | :---: | :---: |
|name|字符串|Static|***唯一**控件名|
|pos|布局定位|0,0|控件位置|
|width|正整数|0|控件宽度|
|height|正整数|0|控件高度|
|size|两个正整数|0,0|控件宽高|
|*background|1/0|0|是否属于窗口背景|
|disable|1/0|0|是否禁用|
|visible|1/0|1|是否可见|
|alpha|0-255整数|255|透明度|
|bordercolor|颜色|black|边框颜色|
|bordersize|非负整数|0|边框宽度|

注：一些控件名应避免使用[默认按钮](UIButton.md)  
*注：如果值为1将不会响应鼠标事件，视作dlg的事件处理，且重绘仅在窗口背景重绘时发生。

* * * * *

|函数名|说明|
| :---: | :---: |
|GetName|获取控件名|
|SetPos|设置控件位置|
|GetPos|取得控件位置|
|GetWidth|获取宽度|
|GetHeight|获取高度|
|AttachBackground|附加至窗口背景|
|DisableCtrl|禁用控件|
|VisibleCtrl|显示控件|
|SetAlpha|设置Alpha值|
|GetAlpha|获取Alpha值|
|SetBorderSize|设置边框宽度|
|GetBorderSize|获取边框宽度|
|SetBorderColor|设置边框颜色|
|GetBorderColor|获取边框颜色|