# 验证结果

- 当程序满足属性时，Ceagle输出`TRUE`
- 当程序不满足属性时，Ceagle输出`FALSE`，并生成`example.c.ce`反例文件
  - 反例文件格式请参阅[http://sv-comp.sosy-lab.org/2016/witnesses/](http://sv-comp.sosy-lab.org/2016/witnesses/)
- 当出现异常时，Cegle输出`UNKNOWN`并给出异常的原因
