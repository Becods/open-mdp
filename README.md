# open-mdp 简介

maimai-diff-predictor 项目旨在通过通用的基于 simai 语法的 majdata.txt 谱面文件，使用经过训练的 lstm 模型进行分析得到推测的谱面定数。

一个在 web 上运行的该项目可见 [https://right-sg.icu/mdp-web](https://right-sg.icu/mdp-web)。

当前版本的项目于 2024/8/24 上传，模型完成于 2024/8/17。目前先开源了模型文件和推理模块，在进一步完善后训练模块也会一同放出。

`inference` 目录下存放了模型的推理模块，可以使用相应程序和模型完成定数推测。

`serializer` 目录下存放了谱面序列化预处理模块，其中 Process 脚本基于 MajdataEdit 项目。

目前项目尚未面向较易用的场景，因此如果需要适应不同需求请查看并修改 `inference` 与 `serializer` 下的源代码从而构建贴合需求的程序。

目前而言，您需要将 `majdata.txt` 放到 `serializer` 目录下并运行 exe 程序，将得到的 `pre-rawchart.json` 文件移动到 `inference` 目录下，再运行 `main.py` 完成推理。显然，要应对大量谱面处理的情况，您有必要需要修改源代码，对应的函数均做了一定程度的封装，因此相关的过程并不繁琐。

目前模型较为稚嫩，预测定数仅供参考，如果有准确度要求请务必辅以人工检查。
