#验证引擎参数

- `--engine=dfs`: 指定验证引擎，可以选择dfs引擎或rewrite引擎
- `--advisor=simple`: 当使用dfs引擎时，指定Advisor的算法，可以选择naive、simple、absref、compositional等算法及其组合
- `--advisor.bmc=200`: 当使用naive或simple算法时，指定bmc展开的深度
- `--advisor.predicate`: 当使用absref算法时，手动指定初始谓词
