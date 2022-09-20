+++
date = "2010-05-15T21:52:57-07:00"
title = "LibreOS"
image = "libreos2.png"
alt = "Rugged Fellows Guide - men's lifestyle Wordpress blog"
color = "#cee5fc"
link1 = ""
link2 = ""

+++

By Jiuming Jiang and Fangxi Han | Key Words: Operation System, C++, Assembly

![68747470733a2f2f73312e617831782e636f6d2f323032322f30332f32322f714b647a38412e706e67](https://linton-pics.oss-cn-beijing.aliyuncs.com/uPic/68747470733a2f2f73312e617831782e636f6d2f323032322f30332f32322f714b647a38412e706e67.png)

### Introducing LibreOS

![image-20220919165107267](https://linton-pics.oss-cn-beijing.aliyuncs.com/uPic/image-20220919165107267.png)

实现了显存管理和简单的用户界面。

实现了多进程，在汇编层面探究了系统调用的原理，可以随意增加自定义系统调用，例如hello系统调用。之后，实现了常见的系统调用，例如join、exit、yield等。

我通过对文件头的复用，实现了目录文件、设备文件等新文件类型的扩展，实现了文件目录树。

同时，我修改文件头结构，调整头大小，为文件添加更加细节信息，例如可以记录文件类型、文件大小、文件权限等额外信息（多用户和访问控制系统暂未实现）。

另外，我在文件头分配时增加了额外机制，当文件头不足以记录这个文件占用的所有文件块时，实现分配附加文件头。如果文件很大，那么它可以由很多个磁盘块构成其文件头，而不局限于之前的单块结构了。这些磁盘块之间采用隐式链接方式组织（每个文件头块有指向下一个文件头块的指针），于是，就可以突破由于文件头不够到导致的文件大小限制问题。

Implemented video memory management and a simple user interface.

Implemented multi-process, explored the principle of system calls at the assembly level, and can add custom system calls at will, such as the hello system call. After that, common system calls such as join, exit, yield, etc. are implemented.

Through the multiplexing of the file header, I realized the expansion of new file types such as directory files and device files, and realized the file directory tree.

At the same time, I modified the file header structure, adjusted the header size, and added more detailed information to the file. For example, additional information such as file type, file size, and file permissions can be recorded (multi-user and access control systems have not been implemented yet).

In addition, I added an additional mechanism to the allocation of file headers, when the file header is not enough to record all the file blocks occupied by this file, the implementation of the allocation of additional file headers. If the file is large, it can consist of many disk blocks to form its file header, instead of being limited to the previous single-block structure. These disk blocks are organized by implicit linking (each file header block has a pointer to the next file header block), so the file size limit problem caused by insufficient file headers can be overcome.

![image-20220919170831068](https://linton-pics.oss-cn-beijing.aliyuncs.com/uPic/image-20220919170831068.png)

![image-20220919170918178](https://linton-pics.oss-cn-beijing.aliyuncs.com/uPic/image-20220919170918178.png)

### Shell Commands

| Command | Usage                                                        | 解释                                                         |
| ------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| cd      | 切换工作路径                                                 | change work path                                             |
| pwd     | 打印当前工作目录                                             | print the current working directory                          |
| mkdir   | 创建目录                                                     | Create a directory                                           |
| touch   | 创建文件                                                     | Create a file                                                |
| rm      | 删除文件或目录                                               | delete file or directory                                     |
| quit    | 退出操作系统                                                 | Exit the operating system                                    |
| ls      | 列出当前目录下的目录、设备或文件（-la可以输出详细文件信息和统计信息） | List directories, devices or files in the current directory (-la can output detailed file information and statistics) |
| ap      | append                                                       | append                                                       |
| hap     | half append                                                  | half append                                                  |
| disk    | 列出磁盘情况                                                 | List disk conditions                                         |

### Read More

| Click the links below to read more about the project.        |
| ------------------------------------------------------------ |
| [[Source Code]](https://github.com/JustLinton/libreos_nachos) |

