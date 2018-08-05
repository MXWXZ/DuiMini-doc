# 环境和项目设置

## 编译环境

DuiMini采用**VS2017**建构，其他编译器需要**C++17**支持，预设置了一些常用的环境，更低版本的VS可以自行转换，相关兼容性问题请自行解决。配置可以参考下表：

| 解决方案配置 | 字符集 | 配置类型 | 平台工具集 |
| :---: | :---: | :---: | :---: |
| Debug | MBCS | 动态库 | V141\_xp |
| Debug-Unicode | Unicode | 动态库 | V141\_xp |
| Release | MBCS | 动态库 | V141\_xp |
| Release-Unicode | Unicode | 动态库 | V141\_xp |
| Release-Static | MBCS | 静态库 | V141\_xp |
| Release-StaticUnicode | Unicode | 静态库 | V141\_xp |

{% hint style="danger" %}
由于代码中使用了部分C++17特性，如果使用不支持的编译器，可能导致内存泄漏等问题。 
{% endhint %}

{% hint style="warning" %}
本库的测试只会在`Debug-Unicode`或`Release-Unicode`配置下进行，不保证其他配置没有兼容性问题，请自行解决或报告给我们。
{% endhint %}

## 运行环境

DuiMini的程序最低支持系统为windows xp，2K及以下系统部分特性可能不支持。完整测试仅在windows 10中进行，xp下如果出现问题请提交issue或自行解决。

## 文件编码

DuiMini采用UTF-8格式保存，XML文件请也采用**UTF-8**保存以正常读取。

## 代码规范

DuiMini遵循[Google开源项目风格指南（C++）](http://zh-google-styleguide.readthedocs.io/en/latest/google-cpp-styleguide/contents/)的相关风格指导，如果希望参与开发，请保持风格统一。

