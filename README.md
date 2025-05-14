# 智能RAG问答系统

这是一个基于RAG（检索增强生成）技术的智能问答系统，使用FastAPI作为后端，React作为前端。

## 环境要求

- Python 3.8+
- Node.js 16+
- npm 8+
- Ollama（用于运行nomic-embed-text模型）

## 安装步骤

### 1. 安装Ollama

首先需要安装Ollama，这是运行嵌入模型所必需的：

1. 访问 [Ollama官网](https://ollama.ai/) 下载并安装
2. 安装完成后，运行以下命令下载nomic-embed-text模型：

```bash
ollama pull nomic-embed-text
```

### 2. 后端设置

1. 创建并激活Python虚拟环境：

```bash
# 创建虚拟环境
python -m venv venv

# 激活虚拟环境
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate
```

2. 安装Python依赖：

```bash
pip install -r requirements.txt
```

3. 创建环境变量文件：
   在项目根目录创建`.env`文件，添加以下内容：

```
DEEPSEEK_API_KEY=your_api_key_here
```

请将`your_api_key_here`替换为您的DeepSeek API密钥。

### 3. 前端设置

1. 进入前端目录：

```bash
cd frontend
```

2. 安装Node.js依赖：

```bash
npm install
```

## 运行项目

### 1. 启动后端服务

1. 确保在项目根目录下
2. 确保虚拟环境已激活
3. 运行以下命令：

```bash
cd backend
python main.py
```

后端服务将在 http://localhost:8000 启动

### 2. 启动前端服务

1. 打开新的终端窗口
2. 进入前端目录：

```bash
cd frontend
```

3. 运行以下命令：

```bash
npm start
```

前端服务将在 http://localhost:3000 启动

## 使用系统

1. 打开浏览器访问 http://localhost:3000
2. 在输入框中输入您的问题
3. 点击"提交问题"按钮
4. 等待系统返回答案

## 常见问题解决

### 1. 后端启动失败

- 检查Python虚拟环境是否已激活
- 检查所有依赖是否已正确安装
- 检查`.env`文件中的API密钥是否正确

### 2. 前端启动失败

- 检查Node.js版本是否符合要求
- 检查是否所有依赖都已正确安装
- 检查端口3000是否被占用

### 3. 问答功能不工作

- 检查后端服务是否正常运行
- 检查Ollama服务是否正常运行
- 检查网络连接是否正常

## 项目结构

```
项目根目录/
├── backend/
│   └── main.py          # 后端主程序
├── frontend/
│   ├── src/
│   │   ├── App.tsx     # 前端主组件
│   │   └── App.css     # 样式文件
│   └── package.json    # 前端依赖配置
├── requirements.txt    # 后端依赖配置
└── .env               # 环境变量配置
```

## 注意事项

1. 确保Ollama服务始终运行
2. 保持API密钥的安全性，不要泄露
3. 首次运行时，系统会自动下载和初始化必要的模型
4. 如果遇到性能问题，可以调整`main.py`中的文本分割参数

## 技术支持

如果遇到问题，请检查：

1. 所有服务是否正常运行
2. 环境变量是否正确配置
3. 网络连接是否正常
4. 控制台是否有错误信息

## 许可证

MIT 
