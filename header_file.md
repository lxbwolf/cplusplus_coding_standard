##### 引用顺序

* .cpp对应的头文件
* &lt;分隔&gt;
* c系统文件
* &lt;分隔&gt;
* c++系统文件
* &lt;分隔&gt;
* QT库文件
* &lt;分隔&gt;
* 公用.h文件
* &lt;分隔&gt;
* 模块.h文件

各部分按字母升序排列

##### 引用路径

按照项目源代码目录树结构排列, 避免使用 UNIX 特殊的快捷目录 . \(当前目录\) 或 .. \(上级目录\).   
`#include "rplcc/header.h"`

##### \#define 保护

所有头文件都应该使用 \#define 来防止头文件被多重包含, 命名格式:  
`<NAMESPACE>_<FILE>_H`

为保证唯一性, 头文件的命名应该基于所在项目源代码树的全路径. 例如, 项目 foo 中的头文件 foo/include/bar/baz.h 可按如下方式保护:

```c
#ifndef BAR_BAZ_H
#define BAR_BAZ_H
…
#endif // BAR_BAZ_H
```

##### 前置声明

能使用前置声明的就不要引用头文件

