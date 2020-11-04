---
title: VSCode中launch.json的介绍
time: 2020-09-07 16:23:04
---
launch.json配置文件介绍
=====
1. `"version"`是Debug的版本；
2. `"configurations"`是个数组，每个项都是一个配置项；
3. `"type" "requeset" "name"`是通用配置项，无论哪个编程语言的调试都需要配置这几项；
4. `"type"`指定的是编程环境，`"name"`是给调试项起一个名字，在Debug中的下拉选项显示，`"request"`是调试模式，调试模式包括`launch`和`attach`；
5. `launch`是vscode负责启动程序并给程序搭配一个调试器，`attach`是为一个已经在运行且暂不支持调试的程序加一个调试器。