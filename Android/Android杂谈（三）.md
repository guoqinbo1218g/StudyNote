# Android 杂谈（三）

## `<merge>` 的使用场景

1. 布局顶结点是 FrameLayout 且不需要设置`background`或`padding`等属性，可以用`merge`代替，因为 Activity contentView 的父布局就是个 FrameLayout ，所以可以用`merge`消除只剩一个。

2.  某布局作为子布局被其他布局`include`时，使用merge当作该布局的顶节点，这样在被引入时顶结点会自动被忽略，而将其子节点全部合并到主布局中。

## 深拷贝的实现方式

1. 重写每个对象的 `Clone()` 方法

2. 通过序列化和反序列化实现。

## 在 Activity 中获取字符串的方式

```java
getString(R.string.app_name);
getResources().getString(R.string.app_name);
Resources.getSystem().getString(R.string.app_name);
```
