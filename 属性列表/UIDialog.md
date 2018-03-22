对话框  
xml名：dlg  
基类：[UIContainer](属性列表/UIContainer.md)

|属性|合法值|默认值|说明|
| :---: | :---: | :---: | :---: |
|title|语言字符串||窗口标题|
|appwin|1/0|1|显示任务栏图标|
|caption|布局定位|0,0,-0,-0|允许拖动窗口的矩形区域|
|movable|1/0|1|允许移动窗口|
|sizebox|4个非负整数|0,0,0,0|缩放边框宽度（左上右下）|
|resizable|1/0|0|允许改变窗口大小|
|alpha|0-255整数|255|窗口Alpha值|
|minwidth|非负整数|0|最小宽度|
|maxwidth|非负整数|窗口宽度（除任务栏）|最大宽度|
|minheight|非负整数|0|最小高度|
|maxheight|非负整数|窗口高度（除任务栏）|最大高度|

- dlg的pos属性在初始化时相对于屏幕，可使用所有前缀标识符！程序运行时则修改为相对于窗口。

* * * * *

|函数名|说明|
| :---: | :---: |
|SetTitle|设置任务栏标题|
|GetTitle|取得任务栏标题|
|ShowTaskBar|显示任务栏|
|AllowWindowMove|允许窗口移动|
|AllowWindowResize|允许改变窗口大小|
|SetSizeBox|设置缩放边框宽度|
|GetSizeBox|获取缩放边框宽度|
|SetCaptionRect|设置允许拖动窗口的矩形区域|
|GetCaptionRect|获取允许拖动窗口的矩形区域|
|SetAlpha|设置窗口Alpha值|
|GetAlpha|获取窗口Alpha值|
|SetMinWidth|设置最小宽度|
|GetMinWidth|获取最小宽度|
|SetMaxWidth|设置最大宽度|
|GetMaxWidth|获取最大宽度|
|SetMinHeight|设置最小高度|
|GetMinHeight|获取最小高度|
|SetMaxHeight|设置最大高度|
|GetMaxHeight|获取最大高度|
