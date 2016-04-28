# 验证属性参数

- `--property-file`: 指定属性文件
- `--property.memory.free`: 指定验证内存释放安全属性
- `--property.memory.defer`: 指定验证内存无野指针属性
- `--property.memory.memtrack`: 指定验证内存无泄漏属性
- `--property.termination`: 指定验证程序终止性
- `--property.overflow`: 验证整数溢出
- `--property.assert`: 验证assert，默认开启
- `--property.reach=file:line`: 验证file文件的第line行可达
