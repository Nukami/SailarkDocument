# SailarkDocument
  这个仓库被用于记录Sailark的一些设计思路与开发文档。
  
# 关于 Sailark
  Sailark在计划中被设计成一个跨平台的工作平台, 它将使用QT(C++)进行开发, 并运行于x86和x64架构的Windows和Linux平台下。  
  它提供了命令行, 系统日志, 图形界面等基本功能。
  Sailark的目的是为了提高生产效率，核心功能是**数据的聚合、快速检索、可视化与分析**。
  在计划中，Sailark将会被用于：
  + 创建个人知识库，用户可以在Sailark中新建一个document，记录自己新get的知识，保存一篇暂时不想看但觉得将来会用到的文章，个人日记，工作日记等等。并基于这些document建立索引，知识图谱等，方便用户浏览检索。
  + 网络收藏夹，浏览历史
  + 个人账号密码管理
  + 数据集的收录与检索
  + 数据可视化与分析
  + 其它为工作生产环境提供的功能插件
  
  
# 快捷访问
  Sailark为用户提供了一个快捷访问的桌面工具，通过快捷键呼出桌面工具后，在快捷访问工具中输入指令或关键词快速或查询。
  
# 插件化模式
  为了使Sailark更灵活与更具可扩展性，我们使用了插件化模式来设计开发Sailark，在插件化模式里，每个功能模块会被作为一个插件存在，我们为每一个功能编写代码，将其编译成一个dll或so文件，当Sailark启动时将会开始加载这些插件来丰富它的功能。  
  在Sailark的插件目录下创建子目录作为各个插件的工作目录，将插件的可执行文件放在工作目录下，移除插件时只需将工作目录删除即可。  
  要注意Sailark的核心功能也是作为模块被封装在插件中的。
