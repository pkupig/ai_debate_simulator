这是一个基于大语言模型 (LLM) 的辩论模拟系统，支持人类玩家参与辩论并实时评分。系统模拟真实辩论流程，包含立论、质询、自由辩论和结辩四个阶段，支持 AI 裁判评分功能。

**系统结构**:
```bash
├── README.md
│
├── main.py
│
├── agents/
│ ├── init.py
│ ├── base_agent.py
│ ├── referee_agent.py
│ ├── debater_agent.py
│ └── player_adapter.py
│
├── utils/
│ ├── init.py
│ ├── knowledge_validator.py
│ ├── speech_handler.py
│ ├── scoring_system.py
│ └── config_loader.py
└── requirements.txt
```

**运行方式**：
```bash
# bash
git clone https://github.com/pkupig/ai_debate_simulator.git
# 需要3.10及以上的python版本
pip install -r requirements.txt
# 确认llm_api密钥已经在系统环境中
# 运行：
python main.py \
  --topic "This is the topic of the debate" \
  --model from[qwen-max, qwen-turbo, qwen-plus] \
  --roles 正方一辩 反方一辩 正方二辩 反方二辩 \
  --player_roles choose which player or team you wanna join in \
  --ai_use use when need
```
