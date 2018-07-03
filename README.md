# Divider
## RecyclerView通用分割线，ItemDecoration for Recyclerview 
##### 适配了LinearLayoutManager、GridLayoutManager、StaggeredGridLayoutManager
# 使用说明：
## Demo
[下载 APK-Demo](https://github.com/Ray512512/divider/blob/master/res/app-debug.apk)
## 效果：
|原始用法|增头增尾|
|:---:|:---:|
|![](https://github.com/Ray512512/Divider/blob/master/res/0.gif)|![](https://github.com/Ray512512/Divider/blob/master/res/1.gif)|

## 导入
### Android studio 
```
implementation 'com.ray:divider:0.0.1'
```
若出现依赖包版本冲突请使用以下依赖方式:
```
compile('com.ray:divider:0.0.1', {exclude group: 'com.android.support'})
``` 
## 调用：
```java
recyclerView.addItemDecoration(Divider.builder()
        .color(Color.BLUE)
        .width(10)
        .height(20)
        .build());
```
## 介绍：
```java
recyclerView.addItemDecoration(Divider.builder()
        .color(Color.BLUE)// 设颜色
        .width(10)// 设线宽px，用于画垂直线
        .height(20)// 设线高px，用于画水平线
        .headerCount(1)// 设头的数量
        .footerCount(1)// 设尾的数量
        .build());
```
// 如果以上属性发生变化，则调用下面对应方法修改
```java
divider.setLineColor(Color.RED);
divider.setLineWidth(30);
divider.setLineHeight(30);
divider.setHeaderCount(2);
divider.setFooterCount(2);
```

## 注意事项：
##### 1.如果增删不是调用的 adapter.notifyDataSetChanged() 则需要调用下面方法重新绘制线
```java
recyclerView.invalidateItemDecorations();
```




        
