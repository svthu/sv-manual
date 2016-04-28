#高级功能

用户在使用Ceagle的高级功能时可能遇到的问题及解决方案

## 什么时候我应该抽象精化选项?
当使用bmc方式求解的策略如路径优先、实时求解无法求解时，可以尝试使用抽象精化。

## 什么时候我应该使用组合验证选项?
程序或项目规模比较大的时候，例如10k行或以上级别的代码。

## 路径优先策略与实时求解策略有什么区别?
路径优先只会在搜索到达了error状态时才回求解路径是否可行，实时求解在搜索过程中的每一步都会求解是否可行。

## 我应该如何选择不同的约束求解器?
默认求解器z3可以解决大部分的问题，对于一些无法求解的问题，可以尝试mathsat或CVC4，对于仅涉及float的问题，可以尝试dReal。