
## 项目介绍
此项目是将`spike`编译成动态链接库用作`difftest`

## 使用介绍

1. 确定编译架构

    在编译前确定将`spike`编译成32bit/64bit的，通过`difftest.cc`里面的`RV32宏和rv64宏来控制`

2. 确定编译名字

    执行`make NAME=32`, 编译后的名字叫做`riscv32-spike-so`

    执行`make NAME=64`, 编译后的名字叫做`riscv64-spike-so`

3. 编译结果 

    编译结果在build目录

- tip
    由于编译的是`spike`，为避免其他因素影响出现bug，所以我们使用`difftest.cc`里面的宏来控制编译位数，并使用`make NAME`来控制名字，而没有使用更简单方便的做法。