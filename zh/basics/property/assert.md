Ceagle支持验证使用C语言中的assert函数声明的安全属性。关于assert函数的使用请参阅C语言的文档和帮助。

Ceagle默认向验证任务添加assert安全属性，如果需要不考虑assert安全属性并忽略所有的assert语句，请对Ceagle进行设置。

## 网页版

## 命令行版

```
# 验证assert，默认开启，该参数可以省略
ceagle --property.assert foo.c

# 属性可以关闭
# 示例如下，验证foo.c中是否有整数溢出，并且关闭默认的assert验证
ceagle --property.assert=false --property.overflow foo.c
```
