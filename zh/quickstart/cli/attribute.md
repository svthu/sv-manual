#添加属性

添加属性有如下方法：

- 修改源代码：在源代码中加入`assert(condition)`，Ceagle会在验证到该行代码时检查`condition`是否为真
- 修改源代码：在源代码中加入一个C语言标枪`ERROR`，Ceagle会验证`ERROR`是否可达
- 通过参数指定代码行：例如在运行时加入`--line=15`，Ceagle会验证第15行是否可达
