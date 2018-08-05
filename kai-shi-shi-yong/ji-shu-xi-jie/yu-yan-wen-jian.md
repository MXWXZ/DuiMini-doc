# 语言文件

{% hint style="warning" %}
请保证`root`为唯一根节点。
{% endhint %}

## 文件格式

```markup
<str name="STR_MAIN_TITLE" value="Demo" />
```

* `name`：标识名
* `value`：翻译字符串

## 使用方法

在"语言字符串"的地方可以用`[langstr]`来表示，例如`title="[STR_MAIN_TITLE]"`  
注：如果你确实要显示类似`[[abc[def]`这样同时以`[`开头，以`]`结尾的字符串，请将第一个`[`修改为`\[`，像这样：`\[[abc[def]`

