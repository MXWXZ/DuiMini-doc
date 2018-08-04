# UIWindow类
|函数名|说明|
| :---: | :---: |
|Run|创建并显示对话框|
|Create|创建窗口|
|ShowWindow|显示隐藏窗口|
|DoModal|模态对话框循环|
|UpdateWindow|重绘窗口|
|GetDialog|取对话框句柄|
|GetHWND|取得窗口句柄|
|SetDlgName|设置dlg名|
|GetDlgName|取得dlg名|
|FindCtrlFromName|按名称查找控件|
|SetWindowPos|设置窗口位置|
|GetWindowPos|取得窗口位置|
|SetWindowSize|设置窗口大小|
|CenterWindow|窗口居中|
|CreateControl|创建控件|
|FinishCreateControl|完成创建控件|
|SetIcon|设置窗口图标|
|Close|关闭窗口|
|Maximize|最大化|
|Restore|还原|
|Minimize|最小化|

* * * * *

窗口类可重载函数（如果不重载请保证响应控件名使用[默认按钮](UIButton.md)）：

|函数名|说明|
| :---: | :---: |
|MsgHandler|截获所有Windows消息|
|OnInit|显示窗口前初始化|
|OnClose|关闭窗口|
|OnMaximize|最大化窗口|
|OnRestore|还原窗口|
|OnMinimize|最小化窗口|