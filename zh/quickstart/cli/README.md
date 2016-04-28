#命令行版

## 下载与安装

- 打开网页浏览器
- 访问Ceagle首页: [http://sts.thss.tsinghua.edu.cn/ceagle](http://sts.thss.tsinghua.edu.cn/ceagle)
- 点击下载按钮，下载ceagle-1.0.zip
- 下载完成后，解压缩下载的压缩包
- 将解压后的目录添加到系统的`PATH`中，例如：
  - 压缩包的路径是`/home/user/ceagle`
  - 编辑用户的`~/.bashrc`文件
  - 在其中加入`export PATH=$PATH:/home/user/ceagle`
- 验证安装：在命令行中输入`ceagle --version`，输出ceagle的命令行帮助则安装成功
    ```
    1.0
    ```

## 添加属性

添加属性有如下方法：

- 修改源代码：在源代码中加入`assert(condition)`或`__VERIFIER_assert(condition)`，Ceagle会在验证到该行代码时检查`condition`是否为真
- 修改源代码：在源代码中加入一个C语言标签`ERROR`，Ceagle会验证`ERROR`是否可达
- 通过参数指定代码行：例如在运行时加入`--line=15`，Ceagle会验证第15行是否可达

例如:
```
// foo.c
#define RATE 0.1

double foo(int a) {
    return a * RATE;
}

double bar(int a) {
    return a / RATE;
}

int main() {
    int nm = 15;
    double r1 = foo(bar(nm)); // 15.0
    double r2 = bar(foo(nm)); // 10.0
    double r3 = foo(bar(nm)); // 15.0
    double r4 = __VERIFIER_nondet_double();
    __VERIFIER_assert(r1 == nm); // safe
    __VERIFIER_assert(r1 != r2); // safe
    __VERIFIER_assert(r1 == r3); // safe
    __VERIFIER_assert(r4 == r4); // unsafe
    return 0;
}

```
## 开始验证

假设目标文件为`foo.c`，在命令行输入`ceagle foo.c`即可验证

## 验证结果

验证结果输入如下:
```
PROPERTY: r1 == nm, RESULT:TRUE
PROPERTY: r1 != r2, RESULT:TRUE
PROPERTY: r1 == r3, RESULT:TRUE
PROPERTY: r4 == r4, RESULT:FALSE
```
