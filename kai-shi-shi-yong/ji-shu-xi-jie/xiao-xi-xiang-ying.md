# 消息响应

## 消息类型

| 消息 | WPARAM/LPARAM参考 | 说明 |
| :---: | :---: | :---: |
| kWM\_MouseEnter | WM\_MOUSEMOVE | 鼠标进入 |
| kWM\_MouseLeave | WM\_MOUSEMOVE | 鼠标离开 |
| kWM\_MouseMove | WM\_MOUSEMOVE | 鼠标移动 |
| kWM\_LButtonDown | WM\_LBUTTONDOWN | 左键按下 |
| kWM\_LButtonUp | WM\_LBUTTONDOWN | 左键弹起 |
| kWM\_LButtonClick | WM\_LBUTTONDOWN | 左键点击 |
| kWM\_LButtonDBClick | WM\_LBUTTONDOWN | 左键双击 |
| kWM\_RButtonDown | WM\_LBUTTONDOWN | 右键按下 |
| kWM\_RButtonUp | WM\_LBUTTONDOWN | 右键弹起 |
| kWM\_RButtonClick | WM\_LBUTTONDOWN | 右键点击 |
| kWM\_RButtonDBClick | WM\_LBUTTONDOWN | 右键双击 |
| kWM\_Disable | NULL | 控件被禁用 |
| kWM\_Invisible | NULL | 控件被隐藏 |
| kWM\_Active | NULL | 控件被启用 |
| kWM\_Visible | NULL | 控件被显示 |
| kWM\_SkinChange | 原skinid&新skinid | 皮肤改变 |
| kWM\_LangChange | 原langid&新langid | 语言改变 |

{% hint style="info" %}
一些默认窗口消息响应参见[UIWindow类](../shu-xing-lie-biao/uiwindow-lei.md#ke-zhong-zai-han-shu)
{% endhint %}

{% hint style="warning" %}
一些控件名应避免使用[默认按钮](../shu-xing-lie-biao/uibutton.md#mo-ren-an-niu)
{% endhint %}

## 截获windows消息

继承自`UIWindow`的窗口类可以重载`MsgHandler`函数截获Windows消息（注意结束时要调用`UIWindow`的`MsgHandler`函数），参考Demo的MainDlg类：

* 声明

  {% code-tabs %}
  {% code-tabs-item title="MainDlg.h" %}
  ```cpp
  protected:
        // override message handler sample
        LRESULT MsgHandler(UINT v_msg, WPARAM v_wparam, LPARAM v_lparam) override;
  ```
  {% endcode-tabs-item %}
  {% endcode-tabs %}

* 定义

  {% code-tabs %}
  {% code-tabs-item title="MainDlg.cpp" %}
  ```cpp
  LRESULT MainDlg::MsgHandler(UINT v_msg, WPARAM v_wparam, LPARAM v_lparam) {
      switch (v_msg) {
      case WM_RBUTTONDBLCLK:
          MessageBox(GetHWND(), _T("Sample of override message handler!"),
                     _T("Demo"), MB_OK);
          break;
      }
      return UIWindow::MsgHandler(v_msg, v_wparam, v_lparam);
  }
  ```
  {% endcode-tabs-item %}
  {% endcode-tabs %}

* 效果 双击右键即可弹出对话框

## 消息绑定

### 静态绑定

* 处理函数格式：

  ```cpp
  bool FuncName(const UIEvent& v_event);
  ```

* 处理函数将会最先执行，返回false则不执行默认处理，返回true执行默认处理。
* 绑定消息\(protected\)

  ```cpp
    MSG_MAP_BEGIN(MainDlg<类名>)
        ON_CONTROL_MSG(_T("name")<控件名>, kWM_LButtonClick<消息名>, FuncName<函数名>);
        ON_PARENT_MSG(UIWindow<父类名>)    // 需要包含父类默认映射时使用
        MSG_MAP_END
  ```

### 动态绑定

* 处理函数格式相同
* 类成员函数（c++11）：

  ```cpp
  BindMsgHandler(控件名, 消息名, std::bind(&类名::函数名, this/类对象, std::placeholders::_1));
  ```

* 普通函数：

  ```cpp
  BindMsgHandler(控件名, 消息名, 函数名);
  ```

* 支持lambda表达式
* 解绑

  ```cpp
  UnbindMsgHandler(控件名, 消息名);
  ```

