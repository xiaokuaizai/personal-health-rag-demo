\# 个人健康档案RAG检索Demo

\## 项目介绍

基于阿里云DashScope Embedding API + OSS普通Bucket，实现健康文档（.txt/.json）上传、向量化、存储与语义检索，支持元数据过滤。



\## 环境配置

1\. 依赖安装：`pip install oss2 dashscope numpy`

2. 测试文件：`test\_blood\_pressure.txt`、`test\_nursing.json`与Notebook同目录



\## 运行步骤

1\. 进入`src/common\_bucket\_demo`，启动Jupyter：`jupyter notebook`

2\. 打开`main.ipynb`，按顺序执行所有单元格

3\. 查看输出：自动完成上传+检索，显示相似度、元数据及原始文本



\## 结果验证

1\. 代码输出：日志显示“成功上传”“检索完成”即为正常

2\. OSS验证：登录阿里云OSS控制台，查看`xkz1` Bucket中是否存在`health\_record\_xxx.json`文件



\## 项目结构

```

personal-health-rag-demo/

├── src/                  # 核心代码目录

│   ├── common\_bucket\_demo/  # 普通Bucket Demo（当前运行代码）

│   │   ├── main.ipynb       # 核心运行文件（完整流程）

│   │   

│   ├── vector\_bucket\_demo/  # 向量Bucket Demo（后续迁移用）

│   │   ├── main.py          # 向量Bucket核心代码模板

│   │   └── vector\_ops.py    # 向量操作工具函数

├── data/                 # 测试数据目录

│   ├── test\_blood\_pressure.txt  # 血压测试文件

│   └── test\_nursing.json       # 护理测试文件

├── docs/                 # 文档目录

│   ├── ai\_collaboration\_log.md  # AI协作简报

├── README.md             # 项目核心说明文档

