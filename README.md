# java小工具平台

## 想法的起因

### 懒

有时候会需要做一些简单的计算或者数据的转化，比如对一个URL做编码/解码，或者计算一个字符串的MD5加密。这时候往往是运行一段自己写的脚本，或者去网上找相关的工具网站。如果能把这些动作都省去，也就是说能让工具集成到一个地方并且能复用，应该会提高效率。

## 功能点

1. 在页面中输入参数，点击执行即可获得输出。（懒得去找）
2. 在页面中即可自定义工具，比如定义入参、工具逻辑代码、依赖的jar包。（懒得开发）
3. 定义新工具后，可以热加载。（懒得部署）

## 实现

### 1.页面实现

用angular4简单搭建了一个SPA页面，在[minitools-frontend](https://github.com/LittleLory/minitools-frontend)中。

### 2.服务端构建

用spring-boot搭建了后端web服务。

### 3.工具类的动态生成

根据页面中定义的入参和逻辑代码，会生成一个函数，然后通过javassist动态生成工具的class文件。

### 4. 依赖包的获取

根据页面中定义的依赖生成pom.xml，执行maven命令，拉取指定jar包到本地。

### 5.工具的热加载

加载工具的class文件和依赖的jar包到ClassLoader。


## 目前进度

基本达到目标。

虽说丑，但是能凑合用。

为什么不把这个坑好好填一填？

因为还不够懒。

以上。