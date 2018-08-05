# UIImage

## 图片

xml名：img  
基类：[UIControl](uicontrol.md)

## 属性

| 属性 | 合法值 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: |
| file | 资源 | - | 图片路径 |
| margin | 布局定位 | 0,0,-0,-0 | 九宫格拉伸区域 |
| mode | [见表](uiimage.md#mode-qu-zhi) | extrude | 图片显示模式 |

### `mode`取值

| 模式名 | 值 |
| :---: | :---: |
| 拉伸 | extrude |
| 平铺（忽略margin属性） | tile |

## 公开函数

| 函数名 | 说明 |
| :---: | :---: |
| SetFile | 改变图片 |
| GetFile | 取图片名 |
| SetMargin | 设置九宫格拉伸区域 |
| GetMargin | 获取九宫格拉伸区域 |
| SetMode | 设置显示模式 |
| GetMode | 取得显示模式 |



