相关规范
========
文件规范
--------
- 文件编码统一使用UTF-8并请确保不出现非ASCII字符。
- 文件换行使用LF格式，git可以配置 ``autocrlf = true`` 自动实现。

代码风格
--------
- 主要风格参见 `Google 开源项目风格指南 <https://zh-google-styleguide.readthedocs.io/en/latest/google-cpp-styleguide/contents/>`_
- 代码格式化使用clang format，VS较高版本可以开启 ``Enable ClangFormat support`` 选项，VSC可以使用插件设置。
- 代码注释使用 `Doxygen风格 <http://www.doxygen.nl/manual/commands.html>`_，便于后期文档生成。

异常处理
--------
- 除第三方库以外，禁用C++异常处理。
- 请采用 ``UIException`` 类处理异常，具体请参考头文件实现。

跨平台相关
----------
- 请尽量减少平台相关代码或做分别处理。
- 时刻注意数据类型长度（包括但不限于long等）

注释规范
--------
- 代码注释统一使用英文，防止乱码等其他问题。
- 文件开头需添加版权信息和作者等（参考已有文件）。

文档更新
--------
- 功能修改后需更新本文档，但代码注释优先级更高。

第三方库
--------
- 使用第三方库需注意尽量挑选轻量级、单一功能的库以免造成体积膨胀（如禁用boost库）。
- 第三方库不能采用GPL等不允许商业/闭源的许可证。
- 由于DuiMini是跨平台的，所以请确保第三方库也是跨平台的。
- 请采用cmake管理第三方库以做到自动化编译。
