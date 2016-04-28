属性文件里可以指定全部5种类型的属性，使用类似于LTL的语句来描述，`init(foo())`指代程序的验证入口为`foo()`函数（一般情况下即`main()`函数）。

5类属性的描述规则如下：

```
# 内存安全属性
# 从上到下依次为内存释放安全、内存无野指针和内存无泄露
CHECK( init(main()), LTL(G valid-free) )
CHECK( init(main()), LTL(G valid-deref) )
CHECK( init(main()), LTL(G valid-memtrack) )
```

```
# 程序终止性
CHECK( init(main()), LTL(F end) )
```

```
# 整数溢出
CHECK( init(main()), LTL(G ! overflow) )
```

```
# assert语句
CHECK( init(main()), LTL(G valid-assert) )
```

```
# 代码可达性
# 此属性要求/path/to/file.c的第n行代码必须可达
CHECK( init(main()), LTL(G reachable), /path/to/file.c, line n )
```
