# 变量绑定

{% hint style="warning" %}
当控件名不存在时将返回nullptr并自动记录warning级日志。
{% endhint %}

## 静态绑定:

* 变量声明：

  ```cpp
  UIControl *var;
  ```

{% hint style="info" %}
`UIControl`可替换为其他控件类
{% endhint %}

* 绑定消息\(protected\)

  ```cpp
  VAR_MAP_BEGIN
  ON_CONTROL_VAR(_T("name")<控件名>,var)
  ON_PARENT_VAR(UIWindow<父类名>)        // 需要包含父类默认映射时使用
  VAR_MAP_END
  ```

## 动态绑定

```cpp
控件类 *var=(控件类*)FindCtrlFromName(_T("name")<控件名>);
```

