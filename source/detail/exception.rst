异常处理
========
DuiMini提供了一个异常处理类 ``UIException`` ，处理和UI库有关的错误。

.. Important:: UI库不处理STL异常，如有需要可以自行捕获。

.. Danger:: UI库函数均保证基本异常安全，但在 ``kEL_Error`` 级别错误发生后将不再保证安全。

错误级别
--------
============  ===============
   名称           说明 
============  ===============
kEL_Normal    无错误
kEL_Warning   警告
kEL_Error     错误（结束进程）
============  ===============

.. Note:: ``kEL_Error`` 级别错误因为无法保证程序安全性或无法继续执行，将会自动以1的返回码退出。

如何使用
--------
.. Tip:: 错误信息列表每次调用都会清空之前的错误信息。

- 设置异常： ``UISetError``
- 获取错误信息列表： ``UIGetErrorMsgList``
- 设置自定义处理函数： ``UIException::SetExtraFunc``

  函数原型（返回true代表已经处理完异常，无需进行其他处理）::

    typedef std::function<bool(int level, const char* msg)> ExtraFunc;

