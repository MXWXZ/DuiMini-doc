config主配置文件
================
初始化
-------
加载配置文件::
    
    UIConfig::LoadConfig(path);
    
默认为 ``config.xml`` 文件。

.. Important:: 请保证 ``root`` 为唯一根节点。

DLG设置
--------
每个dlg配置文件均需在这里注册。
::

    <res type="dlg" name="main" file="xml/main.xml" />

- ``name``：唯一，dlg注册名
- ``file``：xml文件名

皮肤设置
--------
每套皮肤均需在这里注册，分为系统皮肤和一般皮肤，系统皮肤在更换皮肤后依然保持原样，一般皮肤之间可以任意更换。
::

    <style type="skin" name="default" value="skin/default" default="1" />
    <style type="skin" name="testskin" value="skin/testskin" />
    <style type="skin" name="system" value="skin/system" system="1" />

- ``name``：唯一，皮肤注册名
- ``value``：皮肤目录路径
- ``system``：默认为0，为1则为系统皮肤（更换皮肤后依然生效，可不唯一）
- ``default``：默认为0，为1则是默认皮肤（**请保留唯一一条作为默认配置**）

.. Note:: 当 ``system`` 属性为 ``1`` 时 ``default`` 属性将被强制设为 ``0``

语言设置
--------
.. Danger:: 请保证语言设置在字体设置之前！否则字体设置时找不到语言将会报错！

DuiMini支持多语言，每种语言均需在这里注册语言文件。
::

    <res type="lang" lang="zh-cn" file="string/zh-CN.xml" default="1" />
    <res type="lang" lang="en-us" file="string/en-US.xml" />

- ``name``：唯一，语言注册名（建议使用语言代码）
- ``file``：xml文件名
- ``default``：默认为0，为1则是默认语言（**请保留唯一一条作为默认配置**）

字体设置
--------
可为每种语言设置不同的字体。
::

    <style type="font" lang="zh-cn" name="default" file="font/yahei.ttc" size="12" default="1" />
    <style type="font" lang="en-us" name="default" file="font/segoe.ttc" size="12" default="1" />

- ``lang``：对应语言注册名
- ``name``：同一语言内唯一，字体注册名
- ``file``：字体文件路径
- ``size``：像素值
- ``default``：默认为0，为1则是 **当前语言** 下的默认字体（请为 **每个语言** 保留唯一一条作为默认配置）

字号参考
^^^^^^^^^
========= ====== =======
 中文字号   磅数   像素值
========= ====== =======
  八号      5      6 
  七号      5.5    7 
  小六      6.5    8 
  六号      7.5    10
  小五      9      12
  五号      10.5   14
  小四      12     16
  四号      14     18
  小三      15     20
  三号      16     21
  小二      18     24
  二号      22     29
  小一      24     32
  一号      26     34
  小初      36     48
  初号      42     56
========= ====== =======

