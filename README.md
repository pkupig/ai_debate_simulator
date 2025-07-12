这是一个支持人类玩家参与并实时评分的辩论模拟系统。系统模拟真实辩论流程，包含以下四个阶段：

立论
质询
自由辩论
结辩
系统支持 AI 裁判评分功能。

系统结构
深色版本
├── README.md
│
├── main.py
│
├── agents/
│   ├── __init__.py
│   ├── base_agent.py
│   ├── referee_agent.py
│   ├── debater_agent.py
│   └── player_adapter.py
│
├── utils/
│   ├── __init__.py
│   ├── knowledge_validator.py
│   ├── speech_handler.py
│   ├── scoring_system.py
│   └── config_loader.py
└── requirements.txt
运行方式
bash
深色版本
# 1. 克隆仓库
git clone https://github.com/pkupig/ai_debate_simulator.git

# 2. 确保 Python 版本为 3.10 或以上
# 3. 安装依赖
pip install -r requirements.txt

# 4. 设置 LLM API 密钥到系统环境变量
# 5. 运行程序
python main.py \
  --topic "This is the topic of the debate" \
  --model [qwen-max, qwen-turbo, qwen-plus] \
  --roles 正方一辩 反方一辩 正方二辩 反方二辩 \
  --player_roles [选择参与的角色或团队] \
  --ai_use [需要时启用]
参数说明
参数名	说明
--topic	辩论主题
--model	使用的 LLM 模型（可选：qwen-max, qwen-turbo, qwen-plus）
--roles	定义角色（如：正方一辩、反方一辩等）
--player_roles	选择玩家参与的角色或团队
--ai_use	是否启用 AI 功能
文件说明
agents/ 目录
base_agent.py：代理基础类
referee_agent.py：裁判代理逻辑
debater_agent.py：辩手代理逻辑
player_adapter.py：玩家适配器
utils/ 目录
knowledge_validator.py：知识验证工具
speech_handler.py：辩论内容处理模块
scoring_system.py：评分系统实现
config_loader.py：配置加载器
依赖管理
requirements.txt：项目依赖列表，通过 pip install -r requirements.txt 安装
