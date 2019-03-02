编译环境
========
DuiMini支持跨平台，Windows/Linux/MacOS均可运行，cmake请使用3.8以上的版本。

由于时间原因，本地测试环境为：

- Windows 10 with Visual Studio 2017, cmake 3.13.2
- Ubuntu 18.04 with GCC 7.3.0, cmake 3.10.2
- OSX 10.14 with Apple LLVM 10.0.0, cmake 3.13.4

CI环境：

- Windows 10 with MSBuild 15.9.20, cmake 3.12.3
- Ubuntu 16.04 with GCC 5.4.0, cmake 3.12.4

.. Warning:: OSX系统动态链接需要 `特殊设置 <https://www.sfml-dev.org/tutorials/2.5/start-osx.php>`_。

如果有兼容性问题请提交issue。

请使用现代编译器编译，编译器需支持C++11标准。相关版本支持情况请参阅 `cppreference <https://en.cppreference.com/w/cpp/compiler_support>`_。
