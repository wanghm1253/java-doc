# JVM


* xx.java -> javac -> classFile -> classLoader -> metadata
* new一个对象：metadata.class -> 执行引擎 -> 堆heap
* 线程：程序计数器、vmStack、本地方法栈

## class规范

* magic = CAFABEBE开头  4位
* minor version 2位 通常为0
* major version 2位 版本兼容
等等
* javap -v xx.class
* jclasslib Bytecode Viewer
  * 一般信息
  * 常量池
  * 接口
  * 字段
  * 方法
  * 属性
* integer自动装箱的上下限-128~127从缓存返回
* invokeStatic
* invokeDynomic
* invokeVirtual

## 类加载

* 每个类加载器对加载过的类保持一个缓存
* 双亲委派机制，向上委托查找，向下委托加载
  * appClassCloader(项目目录)
  * extClassLoader
  * bootstrapClassLoader（rt.jar）
* 沙箱保护机制
  * java.xxx开头的类不能定义




