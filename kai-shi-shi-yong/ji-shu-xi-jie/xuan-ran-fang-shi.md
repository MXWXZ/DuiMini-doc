# 渲染方式

## 支持方式

DuiMini暂时支持下列渲染方式：

| 方式 | 值 |
| :---: | :---: |
| GDI+（默认） | kRM\_GDIPlus |

## 初始化

* 设置渲染方式：`UIRender::SetRenderMode(RenderMode)`
* 初始化：`UIRender::GlobalInit`
* 设置渲染方式同时初始化：`UIRender::GlobalInit(RenderMode)`

{% hint style="warning" %}
`UIRender::SetRenderMode(RenderMode)`仅在初始化之前调用有效，换言之，在初始化以后将不允许修改渲染方式。 
{% endhint %}

{% hint style="info" %}
清理将会在`UISystem::Cleanup`中自动进行
{% endhint %}



