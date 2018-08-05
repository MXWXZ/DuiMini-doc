# 多语言/皮肤切换

DuiMini设计时即支持实时多语言/多皮肤切换

## 单一窗口切换

这种方式不会修改全局显示皮肤/语言，仅切换设置窗口的皮肤/语言，重新打开后还原为全局设置。

```cpp
UIWindow::ChangeSkin/ChangeLang(皮肤/语言ID)
```

{% hint style="info" %}
ID值可以通过`FindSkinID`或`FindLangID`获得。
{% endhint %}

## 全局切换

这种方式将会修改全局显示皮肤/语言，并切换所有窗口的皮肤/语言。

```cpp
UISystem::ChangeSkin/ChangeLang(皮肤/语言ID)
```

{% hint style="info" %}
所有方式修改后，调用`UpdateWindow(true);`刷新窗口即可查看效果。
{% endhint %}

