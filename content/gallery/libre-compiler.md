+++
date = "2014-02-17T21:57:17-07:00"
title = "LibreCompiler"
image = "librecompiler2.png"
alt = "Osprey - minimalist blog and portfolio Hugo theme"
color = "#8792f6"
link1 = ""
link2 = ""

+++

By Jiuming Jiang | Key Words: Compiler, Python, C++, Assembly

![68747470733a2f2f73312e617831782e636f6d2f323032322f30332f32322f714b647a38412e706e67](https://linton-pics.oss-cn-beijing.aliyuncs.com/uPic/68747470733a2f2f73312e617831782e636f6d2f323032322f30332f32322f714b647a38412e706e67.png)

### Introducing LibreCompiler

我们实现了一个编译器，可以编译和处理PL0语言，分为预处理、词法分析、语法分析、语义分析、代码优化器和目标代码生成模块。

We implemented a compiler that can compile and process PL0 languages, divided into modules for preprocessing, lexical analysis, syntax analysis, semantic analysis, code optimizer, and object code generation.

![image-20220919172206434](https://linton-pics.oss-cn-beijing.aliyuncs.com/uPic/image-20220919172206434.png)

### What We Did

实现代码预处理，完成关键字、标识符、数字、操作符等的识别，并输出各lexeme的全程量：SYM和NAME。

然后构建SLR自动机，按翻译模式完成语法分析，在该过程中生成符号表和四元式，按格式输出。

为方便实现，我们利用递归下降分析直接生成符合实验要求的目标代码。若遇标识符，则去查看符号表,看是否有过正确的定义。

代码生成后，利用解释器对目标代码进行模拟执行，并对执行结果进行评估。

Implement code preprocessing, complete the identification of keywords, identifiers, numbers, operators, etc., and output the full amount of each lexeme: SYM and NAME.

Then construct the SLR automaton, complete the syntax analysis according to the translation mode, generate the symbol table and quaternion in the process, and output according to the format.

![image-20220919172445364](https://linton-pics.oss-cn-beijing.aliyuncs.com/uPic/image-20220919172445364.png)

For the convenience of implementation, we use recursive descent analysis to directly generate the target code that meets the experimental requirements. If you encounter an identifier, go to the symbol table to see if there is a correct definition.

After the code is generated, the interpreter is used to simulate the execution of the target code, and the execution result is evaluated.

### Read More

| Click the links below to read more about the project.        |
| ------------------------------------------------------------ |
| [[Source Code]](https://github.com/JustLinton/libre-compiler) |

