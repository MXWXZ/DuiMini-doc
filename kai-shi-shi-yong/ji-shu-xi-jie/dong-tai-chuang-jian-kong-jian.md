# 动态创建控件

1. 首先申请内存，如：

   ```cpp
    UIImage* new_ctrl = new UIImage;
   ```

2. 然后创建控件，`parent`为父控件指针（父控件必须继承自`IUIContainer`），如果不是创建新窗口，请结合`FindCtrlFromName`设父控件为窗口dialog：

   ```cpp
    CreateControl(new_ctrl, parent);
   ```

3. 接下来便使用`SetAttribute`设置初始属性:

   ```cpp
    new_ctrl->SetAttribute(_T("file"), _T("C:\\demo.png"));
   ```

4. 最后完成创建：

   ```cpp
    FinishCreateControl(new_ctrl);
   ```

5. 手动刷新

   ```cpp
    UpdateWindow();
   ```

6. 释放掉申请的内存 有父控件时可以不释放，对话框销毁时自动释放，但无父控件时必须手动释放：

   ```cpp
    delete new_ctrl;
   ```

{% hint style="info" %}
动态创建的控件如果要绑定消息响应，必须在`FinishCreateControl`之后使用[动态绑定](xiao-xi-xiang-ying.md#dong-tai-bang-ding)的方法进行绑定。
{% endhint %}

