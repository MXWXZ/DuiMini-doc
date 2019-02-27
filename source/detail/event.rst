消息事件
========

所有控件、窗口行为均通过消息事件触发响应。

消息事件通过 ``UIEvent`` 类传递，其中 ``Event`` 枚举定义了支持的消息类型，部分附带了一些参数：

=======================  ================
类型名                    备注
=======================  ================
kEVT_MouseEnter          鼠标进入
kEVT_MouseLeave          鼠标离开
`kEVT_MouseMove`_        鼠标移动
`kEVT_LButtonDown`_      左键按下
`kEVT_LButtonUp`_        左键抬起
`kEVT_LButtonClick`_     左键点击
`kEVT_LButtonDBClick`_   左键双击
`kEVT_RButtonDown`_      右键按下
`kEVT_RButtonUp`_        右键抬起
`kEVT_RButtonClick`_     右键点击
`kEVT_RButtonDBClick`_   右键双击
kEVT_Disable             控件被禁用
kEVT_Active              控件被激活
kEVT_Invisible           控件不可见
kEVT_Visible             控件可见
`kEVT_SkinChange`_       皮肤被改变
`kEVT_LangChange`_       语言被改变
=======================  ================

.. note:: ``kEVT_Active`` 和 ``kEVT_Visible`` 在窗口初始化时依然会被传递（除非设置相应初值为0）。

.. attention:: 当控件被禁用或不可见时类似 ``kEVT_MouseEnter`` 的部分事件会被发送给控件，但是响应函数不会被执行，如有特殊需求请自行截获。

kEVT_MouseMove
--------------
- 参数：鼠标位置
- API：
  ::

    void SetPos(Point v_pt)
    Point GetPos() const

kEVT_LButtonDown
----------------
- 参数：同 `kEVT_MouseMove`_

kEVT_LButtonUp
--------------
- 参数：同 `kEVT_MouseMove`_

kEVT_LButtonClick
-----------------
- 参数：同 `kEVT_MouseMove`_

kEVT_LButtonDBClick
-------------------
- 参数：同 `kEVT_MouseMove`_

kEVT_RButtonDown
----------------
- 参数：同 `kEVT_MouseMove`_

kEVT_RButtonUp
--------------
- 参数：同 `kEVT_MouseMove`_

kEVT_RButtonClick
-----------------
- 参数：同 `kEVT_MouseMove`_

kEVT_RButtonDBClick
-------------------
- 参数：同 `kEVT_MouseMove`_

kEVT_SkinChange
---------------
- 参数：新旧资源ID
- API：
  ::
  
    void SetRes(ResChangeEvent res)
    ResChangeEvent GetRes() const

kEVT_LangChange
---------------
- 参数：同 `kEVT_SkinChange`_
