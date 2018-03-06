## 使用NPP加MinGW编译器开发小型程序:

- NPP
  - 主题：Obsidian+consola+全局字体
  - 下载插件管理 https://github.com/bruderstein/nppPluginManager/releases
    - 两个文件分别放置在plugins和updater文件夹下
  - 安装 NppExec 插件
  - 添加 Execute (需要手动新建compile文件夹)
    - 编译：```cmd /k g++ -o $(CURRENT_DIRECTORY)\compile\$(NAME_PART).exe "$(FULL_CURRENT_PATH)" & PAUSE & EXIT```
    - 编译并运行：```cmd /k g++ -o $(CURRENT_DIRECTORY)\compile\$(NAME_PART).exe "$(FULL_CURRENT_PATH)" &cmd /k "$(CURRENT_DIRECTORY)\compile\$(NAME_PART)" & PAUSE & EXIT```
    - 调试：```gdb $(CURRENT_DIRECTORY)\compile\$(NAME_PART).exe```
  - 设置 Advanced Options 在左侧添加到宏

