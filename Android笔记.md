# Android 教程

## 第一章 Android 基础知识

### 一 创建 Android 程序步骤

1. Project name 项目名
2. SDK 版本 - 2.3 or 4.0
3. Application name APP名
4. Package name 包名
5. Create Activity Activity名
6. Min SDK Version 最低SDK版本

### 二 Android 程序目录

src文件夹：开发者编写的程序源文件

gen文件夹：R.java文件

Android： Android类目录

assets文件夹：资源文件夹

res文件夹：会在R.java文件生成ID的资源文件夹

1. drawable-hdpi文件夹：存放高分辨率图片
2. drawable-ldpi文件夹：存放低分辨率图片
3. drawable-mdpi文件夹：存放中分辨率图片
4. layout文件夹： Activity布局文件
5. values文件夹： 值文件
6. AndroidManifest.xml文件：APP配置文档

### 三 四大组件

1. Activity：负责应用程序当中数据的展示，即活动窗口界面
2. Intent：应用程序当中所有的数据都通过 Intent 传递
3. Service：负责大多数数据处理的工作，不可见
4. Content Provider 负责存储数据，并允许应用程序访问这些数据

### 四 Activity 初步

#### 创建 Activity 要点

1. 一个 Activity 就是一个类，并且这个类要继承Activity
2. 需要复写onCreate方法
3. 每一个Activity都需要在AndroidManifest.xml文件中进行配置
4. 为Activity添加必要的控件