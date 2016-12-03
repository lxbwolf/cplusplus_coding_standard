##### 文件

在每一个文件开头加入版权公告, 和文件内容描述.

##### 类

每个类的定义都要附带一份注释, 描述类的功能和用法. 
如果该类的实例可被多线程访问, 要特别注意文档说明多线程环境下相关的规则和常量使用.

##### 函数

函数声明处注释描述函数功能.
注释位于声明之前, 对函数功能及用法进行描述. 注释使用叙述式 (“Opens the file”) 而非指令式 (“Open the file”); 注释只是为了描述函数, 而不是命令函数做什么.

##### 变量

不能依赖注释解释变量的功能, 而是通过变量自解释

##### 实现

对于代码中巧妙的, 晦涩的, 重要的地方加以注释.
如果需要连续进行多行注释, 可以使之对齐获得更好的可读性:

```c
DoSomething();                  // Comment here so the comments line up.
DoSomethingElseThatIsLonger();  // Comment here so there are two spaces between
                                // the code and the comment.
{
  DoSomethingElse();            // Two spaces before line comments normally.
}
```

不要用自然语言翻译代码作为注释. 要假设读代码的人 C++ 水平比你高, 即便他/她可能不知道你的用意:
```c
// 现在, 检查 b 数组并确保 i 是否存在,
// 下一个元素是 i+1.
...        // 天哪. 令人崩溃的注释.
```

##### TODO

对于临时的, 短期的解决方案, 或已经够好但仍不完美的代码使用 TODO 注释.