# 异常处理

DuiMini提供了一个异常处理类`UIException`

## 错误级别

| 名称 | 说明 |
| :---: | :---: |
| kEL\_Normal | 无错误 |
| kEL\_Warning | 警告 |
| kEL\_Error | 错误（结束进程） |

## 错误码

| 名称 | 说明 | 默认级别 |
| :---: | :---: | :---: |
| kEC\_Success | 无错误 | kEL\_Normal |
| kEC\_FileFail | 文件错误 | kEL\_Error |
| kEC\_ThirdPartFail | 第三方函数错误 | kEL\_Error |
| kEC\_IDInvalid | 标识符不合法 | kEL\_Warning |
| kEC\_FormatInvalid | 格式不合法 | kEL\_Warning |

{% hint style="danger" %}
为了便于管理和异常处理，只允许调高错误级别，因为出现级别为`kEL_Error`错误的函数UI库将默认其必定执行成功。换言之，调低默认异常级别可能会导致内存泄漏、空指针等问题。
{% endhint %}

## 如何使用

* 设置异常：`UISetError`
* 获取最后错误码：`UIGetLastError`
* 获取错误信息：`UIGetLastErrorMsg`
* 设置自定义处理函数：`UIException::SetExtraFunc`

  函数原型（返回true代表已经处理完异常，无需进行默认处理）：

  {% code-tabs %}
  {% code-tabs-item title="Utils\\UIException.h" %}
  ```cpp
  std::function<bool(ErrorLevel v_level, ErrorCode v_code, UStr v_msg)> ExtraFunc;
  ```
  {% endcode-tabs-item %}
  {% endcode-tabs %}



