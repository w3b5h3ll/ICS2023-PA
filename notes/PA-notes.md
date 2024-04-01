成为一名合格的CSer！


# PA0
## Installing Ubuntu
Ubuntu 22.04.4 LTS

- `Download updates while installing Ubuntu` Don't use it
- `Software Updater` >> `Remind Me Later`

Install Goolge Pinyin
- https://www.cnblogs.com/it-Ren/p/15566581.html

## vim configuration
- [ ] more plugins...



GNU diff format: https://www.gnu.org/software/diffutils/manual/html_node/Unified-Format.html

Why STFW?
- Google >> general question
- Wiki >> defination concept
- stack overflow >> programs...



## More Exploration
- [ ] Install tmux
- [ ] The Missing Semester of Your CS Education.


> 对. PA除了让大家巩固ICS理论课的知识之外, 还承担着一个重要的任务: 把大家培养成一个素质合格的CSer. 事实上, 一个素质合格的CSer, 需要具备独立搜索解决方案的能力. 这是IT企业和科研机构对程序员的一个基本要求: 你将来的老板很可能会把一个任务直接丢给你, 如果你一遇到困难就找人帮忙, 老板就会认为你没法创造价值.
> PA在尝试让你重视这些业界和学术界都看重的基本要求, 从而让你锻炼这些能力和心态: 遇到问题了, 第一反应不是赶紧找个大神帮忙搞定, 而是"我来试试STFW和RTFM, 看能不能自己解决". 所以PA不是按部就班的中学实验, 不要抱怨讲义没写清楚导致你走了弯路, 我们就是故意的: 我们会尽量控制路不会太弯, 只要你摆正心态, 你是有能力去独立解决这些问题的. 重要的是, 你得接受现实: 你走的弯路, 都在说明你的能力有待提升, 以后少走弯路的唯一方法, 就是你现在认真把路走下去.



## Source Code
直接从github进行clone
```bash
git clone https://github.com/NJU-ProjectN/ics-pa.git
git checkout 2023


```
> color.ui 是指定颜色显示的设置，true 表示启用颜色显示，让 Git 在命令行界面中以彩色显示输出，这样可以更加直观地查看 Git 输出信息，比如分支、提交记录等。

在获取框架代码之前, 首先请你在github上添加一个ssh key, 具体操作请STFW.
- https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

understand git actions:
- http://onlywei.github.io/explain-git-with-d3

解决下面的报错
```bash
w3b5h3ll@ICS2023-PA:~/ICS2023-PA/ics-pa/nemu$ make menuconfig 
/home/w3b5h3ll/ICS2023-PA/ics-pa/nemu/scripts/config.mk:20: Warning: .config does not exists!
/home/w3b5h3ll/ICS2023-PA/ics-pa/nemu/scripts/config.mk:21: To build the project, first run 'make menuconfig'.
+ CC confdata.c
+ CC expr.c
+ CC preprocess.c
+ CC symbol.c
+ CC util.c
+ YACC build/parser.tab.h
make[1]: bison: No such file or directory
make[1]: *** [Makefile:32: build/parser.tab.h] Error 127
make: *** [/home/w3b5h3ll/ICS2023-PA/ics-pa/nemu/scripts/config.mk:39: /home/w3b5h3ll/ICS2023-PA/ics-pa/nemu/tools/kconfig/build/mconf] Error 2
```
>> install bison flex
A menu will pop up. >> Just `Exit` and `Yes` to save the configuration.

make && make run
产生error
```bash
w3b5h3ll@ICS2023-PA:~/ICS2023-PA/ics-pa/nemu$ make run
/home/w3b5h3ll/ICS2023-PA/ics-pa/nemu/build/riscv32-nemu-interpreter --log=/home/w3b5h3ll/ICS2023-PA/ics-pa/nemu/build/nemu-log.txt  
[src/utils/log.c:30 init_log] Log is written to /home/w3b5h3ll/ICS2023-PA/ics-pa/nemu/build/nemu-log.txt
[src/memory/paddr.c:50 init_mem] physical memory area [0x80000000, 0x87ffffff]
[src/monitor/monitor.c:51 load_img] No image is given. Use the default build-in image.
[src/monitor/monitor.c:28 welcome] Trace: ON
[src/monitor/monitor.c:29 welcome] If trace is enabled, a log file will be generated to record the trace. This may lead to a large log file. If it is not necessary, you can disable it in menuconfig
[src/monitor/monitor.c:32 welcome] Build time: 05:29:26, Apr  2 2024
Welcome to riscv32-NEMU!
For help, type "help"
[src/monitor/monitor.c:35 welcome] Exercise: Please remove me in the source code and compile NEMU again.
riscv32-nemu-interpreter: src/monitor/monitor.c:36: welcome: Assertion `0' failed.
make: *** [/home/w3b5h3ll/ICS2023-PA/ics-pa/nemu/scripts/native.mk:38: run] Aborted (core dumped)
```
>> monitor.c:36
- [ ] fix it in PA1

To debug NEMU with gdb: `make gdb`

### Local Commit
git commit --allow-empty(without this option, git will reject no-change commits)

remember:
- STFW
- RTFM
- RTFSC
https://i.linuxtoy.org/docs/guide/
https://akaedu.github.io/book/



### Q & A
- su认证失败是怎么回事?
- grep提示no such file or directory是什么意思?
- 请问怎么卸载Ubuntu?
- C语言的xxx语法是什么意思?
- ignoring return vaule of 'scanf'是什么意思?
- 出现curl: not found该怎么办?
- 为什么strtok返回NULL?
- 为什么会有Segmentation fault这个错误?
- 什么是busybox?
