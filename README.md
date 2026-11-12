# AI 求职助手（ai-job-hunter）

从零搭建的 AI 求职工具——搜岗位 → 分析 JD → 对比简历 → 给出投递建议。  
7 周渐进式构建，每周都有可运行的产物。

## 技术栈

Python · aiohttp（异步爬虫） · OpenAI/DeepSeek API · LangChain · LangGraph

## 项目结构

```
ai-job-hunter/
├── main.py          # W2: CLI 入口（命令行工具）
├── crawler.py       # W3: 异步爬虫，抓取岗位列表
├── analyzer.py      # W4: LLM 分析岗位需求
├── tools.py         # W5: Function Calling 工具集
├── chain.py         # W6: LangChain 自动化链路
├── agent.py         # W7: LangGraph 自主决策 Agent
├── resume.md        # 你的简历（Agent 读取这个）
├── data/            # 爬取的岗位数据
└── requirements.txt # 依赖清单
```

## 7 周构建计划

| 周 | 主题 | 项目交付物 | 验收标准 |
|----|------|-----------|---------|
| W1 | Git 工作流 | 仓库初始化 + 骨架 | GitHub 可访问，README 清晰 |
| W2 | Python CLI | `main.py` 可接收参数运行 | `python main.py --help` 正常输出 |
| W3 | 异步爬虫 | `crawler.py` 爬岗位数据 | 串行 vs 并行耗时对比有数据 |
| W4 | LLM API | `analyzer.py` 分析 JD | AI 能总结岗位技能要求 |
| W5 | Function Calling | `tools.py` 工具集 | AI 能调用搜索/保存等工具 |
| W6 | LangChain 链 | `chain.py` 全自动链路 | 爬→分析→报告一键完成 |
| W7 | LangGraph Agent | `agent.py` 自主决策 | Agent 根据简历推荐岗位 |

## 环境

- Python 3.11+、uv 包管理
- 大模型 Key 放 `.env`（不提交），从 `.env.example` 复制

## 进度

- [x] W1：项目骨架搭建（2026-10-26）
- [ ] W2–W7 待开始