资源加载
========
.. Warning:: 目前32位平台编译的程序可能不支持2G以上文件加载。

设定资源文件
------------
DuiMini目前支持3种资源加载方式，默认不加载资源：

普通文件
^^^^^^^^
加载普通文件，参数为资源文件根目录。
::

    UIResource::SetResMode(kRT_File, "uires");

- 设定当前目录下的 ``uires`` 目录为资源文件根目录。
- 文件解析时路径为相对根目录路径，如 ``uires/1.txt`` 只需传入 ``1.txt`` 即可。

打包文件
^^^^^^^^
可以将所有资源文件打包为zip格式的压缩包加载。
::

    UIResource::SetResMode(kRT_Package, "res.zip");

- 加载当前目录下的 ``res.zip`` 文件。
- 文件解析时路径为压缩包内的路径，如 ``res.zip`` 中 ``uires/1.txt`` 只需传入 ``uires/1.txt`` 即可。

内存加载
^^^^^^^^
可以将资源文件打包进可执行文件形成单文件，请使用 :doc:`../tool/respacker` 打包文件。
::

    UIResource::SetResMode(kRT_Raw, "Demo.exe");

- 加载 ``Demo.exe`` （自身）中打包的资源文件。
- 文件解析时路径和 `打包文件`_ 相同

解析文件
--------
解析文件需要通过资源解析器获取，您可自定义资源解析器，只需继承自 ``IUILoadFile`` 类即可。

.. Warning:: 资源加载返回智能指针，系统释放时会调用特定函数，请不要手动释放！

普通文件解析
^^^^^^^^^^^^  
::

    auto res = UIResource::LoadRes<UIRawLoader>("1.txt");
    res->GetFile();         // 文件数据指针
    test->GetFileSize();    // 文件大小

自定义解析器
^^^^^^^^^^^^
::

    class CustomLoader : public IUILoadFile {
    public:
        bool LoadFile(const void* buffer, long size) override {
            // do something, DO NOT free buffer!
            return true;    // true for success
        }
    };

使用::

    auto res = UIResource::LoadRes<CustomLoader>("1.txt");