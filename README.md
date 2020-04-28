# Wrapper netty Project

本项目提供如何定制netty的模板，如果你想要在netty中定制化一些底层的逻辑，那么你去直接修改netty的代码，
这通常不是一个好主意，让我们以简单的方式去定制netty，比随时随地更换追踪的内核版本。


## 使用

1. 下载源码,编译执行 
        
        mvn clean install -Dmaven.test.skip=true -Dmaven.javaDoc.skip=true

2. 使用依赖

            <dependency>
                <groupId>com.wrapper.netty</groupId>
                <artifactId>netty-all</artifactId>
                <version>4.1.34-SNAPSHOT</version>
             </dependency>

## 优势

1. 便捷的追踪开源代码方式
    - 避免开发者对netty本身的修改
2. 迭代future吸收
    - 随时随地的吸收bugfix，补丁。不需要和netty官方版本进行绑定。
3. 轻易版本升级
    - 模板控制了netty内核版本（当前4.1.34），提供了一个选项即可完成内核版本的升级。
4. 极小的技术负债
    - 避免人员流动对项目本身造成安全隐患

## 模块介绍

1. netty-all
    - 打包实现
2. netty-common
    - 可选用于定义公共类
3. netty-inner
    - 核心的魔改代码

### netty-inner

inner作为最为核心的模块，本质上通过覆盖的策略，去过滤掉来自netty的类。

1. 魔改后定制你想要向netty的植入逻辑

本工程中为netty中的HttpMessage额外的增加了一个default方法，无实际作用，但是提供了读者参考
对netty进行变更的操作

### 关于使用

同开源版本，仅仅更换坐标即可

## 关于netty特性

请参考社区

## 关于我

java人士一枚，擅长开源定制，技术负债弱化。欢迎交流

![](https://github.com/open-wrapper/netty-wrapper/blob/master/codeL.jpg)


