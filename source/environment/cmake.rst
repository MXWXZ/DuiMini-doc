CMake选项
=========

主要选项
--------
主要选项和默认值如下：

====================  =======  ======================
选项名                 默认值   备注
====================  =======  ======================
BUILD_SHARED_LIBS     OFF      TRUE为动态链接
CMAKE_BUILD_TYPE      Release  默认生成类型
DUI_BUILD_TOOLS       ON       生成DUI工具
DUI_BUILD_TESTS       OFF      生成测试
====================  =======  ======================

.. Warning:: 添加或修改高级选项可能导致生成文件体积变大等情况出现。

高级-SFML选项
-------------
SFML选项相比原版将 ``SFML_BUILD_NETWORK`` 和 ``SFML_BUILD_AUDIO`` 默认值调整为 ``FALSE`` ，如有需要可以自行添加。

关于SFML选项具体细节参见：https://www.sfml-dev.org/tutorials/2.5/compile-with-cmake.php

高级-googletest选项
--------------------
将 ``INSTALL_GTEST`` 默认值调整为 ``FALSE``，``gtest_force_shared_crt`` 在VS中默认值调为 ``TRUE``
