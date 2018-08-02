# CommandLineArgsParse

一个简单的解析命令行参数的扩展

# 使用范例

命令行输入的样例为：

```shell
test.exe -s 1 -e 10 -v
```

使用如下方式解析

```c#
static void Main(string[] args)
{
    var arguments = CommandLineArgumentParser.Parse(args);
    if (arguments.Has("-s"))
    {
        var start = int.Parse(arguments.Get("-s").Next);
    }
    if (arguments.Has("-e"))
    {
        var end = int.Parse(arguments.Get("-e").Next);
    }
    if (arguments.Has("-v"))
    {
       bool t = true;
    }
}
```
