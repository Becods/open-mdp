# 谱面 Serializer 工具简介

存放了基于 MajdataEdit 项目的谱面序列化脚本程序，通过谱面文件 `majdata.txt` 生成初步序列化的 `json` 文件。预编译的 exe 程序可以对应通常的序列化操作，将谱面文件 `majdata.txt` 放在相同目录下即可操作。

如果需要批量处理谱面，可以修改 `src` 中的 `cs` 脚本。注意当前版本的 `cs` 脚本内容不严格对应 exe 的程序，而是用于作为 Subprocess 时使用，针对通常用途的修改可能需要修改的内容较多。

利用该工具初步序列化后，谱面仍然需要在推理前经过 `python` 程序的进一步特征工程生成下一步的序列化 `json` ，详情见 `inference` 侧。

将对应功能完整重写到 python 侧在 Todo List 之中。
