# UIControl
所有控件的基类

|属性|合法值|默认值|说明|
| :---: | :---: | :---: | :---: |
|name|字符串|Static|***唯一**控件名|
|pos|布局定位|0,0|控件位置|
|width|正整数|0|控件宽度|
|height|正整数|0|控件高度|
|size|两个正整数|0,0|控件宽高|
|*bgpaint|1/0|0|是否属于背景重绘|
|**transmouse|见表|none|是否穿透鼠标事件|
|disable|1/0|0|是否禁用|
|visible|1/0|1|是否可见|
|alpha|0-255整数|255|透明度|
|bordercolor|颜色|black|边框颜色|
|bordersize|非负整数|0|边框宽度|
|tooltip|语言字符串||鼠标悬浮tooltip|
|tooltipwidth|正整数|300|tooltip最大宽度|

注：一些控件名应避免使用[默认按钮](UIButton.md)\
*注：若值为1则仅当背景重绘时重绘控件（速度慢），建议不常刷新的设为1以加快非背景重绘刷新速度\
**注：取值见下表
|模式名|值|
| :---: | :---: |
|不穿透|none|
|穿透一层|single|
|穿透到窗口|all|

* * * * *

|函数名|说明|
| :---: | :---: |
|GetName|获取控件名|
|SetPos|设置控件位置|
|GetPos|取得控件位置|
|GetWidth|获取宽度|
|GetHeight|获取高度|
|AttachBgPaint|附加至背景重绘|
|SetTransmouse|设置鼠标穿透模式|
|GetTransmouse|获取鼠标穿透模式|
|DisableCtrl|禁用控件|
|VisibleCtrl|显示控件|
|SetAlpha|设置Alpha值|
|GetAlpha|获取Alpha值|
|SetBorderSize|设置边框宽度|
|GetBorderSize|获取边框宽度|
|SetBorderColor|设置边框颜色|
|GetBorderColor|获取边框颜色|
|SetToolTip|设置tooltip|
|GetToolTip|取得tooltip|
|SetToolTipWidth|设置tooltip最大宽度|
|GetToolTipWidth|取得tooltip最大宽度|