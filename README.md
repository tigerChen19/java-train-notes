# Java训练营笔记
## jvm命令行工具
- **Java**  Java应用的启动程序
- **javac** jdk内置的编译工具
- **javap** 反编译class文件的工具，将class反编译成字节码查看
- **jar** 打包工具，可以将文件和目录打包成.jar文件；.jar文件本质上就是zip文件，只是后缀不同。
- javadoc 根据Java代码和标准注释，自动生成相关的api说明文档
- javah JNI开发时，根据Java代码生成需要的.h文件
- extcheck  检查某个jar文件和运行时扩展jar有没有版本冲突，很少使用
- jdb Java Debugger，很少使用
- jdeps 探测class或jar包需要的依赖
- keytool 安全证书和秘钥的管理工具；支持生成、导入、导出等操作
- jarsigner jar文件签名和验证工具
- policytool  实际上是一款图形界面工具，管理本机的Java安全策略

- **jps/jinfo** 查看Java进程
       
       `-l 显示进程名字   -mlv显示进程详细信息`
- **jstat** 查看jvm内部gc相关信息

       `-gc 显示堆内存的使用情况，kb单位；-gcutil 显示堆内存使用率，百分比`
       `示例：jstat -gc pid 1000 1000 （1000  1000 表示打印1000次，每1秒打印一次）`
       `jstat -gcutil pid 1000 1000`
- **jmap**  查看heap或类占用空间统计

      `-heap 打印堆内存的配置和使用信息`
      `-histo 打印哪些类占用的空间多，直方图`
      `-dump:format=b,file=xxx.hprof导出到文件`
- **jstack**  查看线程信息

      `jstack -l pid`
- **jcmd**  执行jvm相关分析命令（整合命令）

      `jcmd pid help`
      'jcmd pid VM.version
       jcmd pid VM.flags
       jcmd pid VM.command_line
       jcmd pid VM.system_properties
       jcmd pid Thread.print
       jcmd pid GC.class_histogram
       jcmd pid GC.heap_info'
- **jrunscript/jjs**  执行js命令



## Windows控制台窗口拉宽方法
输入命令wmic，然后输入exit。即可

## gc日志输出到文件
-Xloggc:xxx.log

