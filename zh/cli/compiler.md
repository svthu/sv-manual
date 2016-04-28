#编译器参数

指定使用的clang的位置, 默认会使用环境变量中的clang，如果clang的版本不是3.7.0则会尝试使用clang-3.7，如果都无法使用，则会报错，需要手动指定编译器的位置

`--compiler=clang,clang-3.7`: 指定clang，例如`--compiler=/home/user/clang/bin/clang-3.7`
