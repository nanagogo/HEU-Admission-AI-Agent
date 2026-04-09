# HEU-Admission-AI-Agent
“基于 Dify 编排的哈工程招生 Agent，集成意图分流与自动评测机制”
# 🏫 HEU-Admission-AI-Agent (哈工程招生智能代理)
这是一个基于 **Dify** 深度编排的垂直领域 AI Agent 实战项目。针对高校招生咨询中常见的“大模型幻觉”问题，构建了具备意图识别、硬逻辑拦截与自动化评测能力的 RAG 系统。
---
## 🚀 核心架构亮点 (Key Features)
- **意图路由分流 (Intent Routing)**：利用 LLM 节点对用户问题进行分类，精准分发至“招生政策”与“校园生活”不同处理分支。
- **事实忠实度严控 (Hallucination Mitigation)**：通过 If/Else 条件分支，在知识库检索结果为空或置信度低时，强制触发人工热线/官网链接的兜底模板，物理阻断幻觉生成。
- **自动化评测闭环 (LLM-as-a-Judge)**：引入 GPT-4o 作为并行裁判节点，通过跨节点变量聚合，实现对生成结果的“事实一致性”实时审计。
## 📂 项目结构
- `高校招生智能问答系统-RAG实战.yml`: Dify 工作流 DSL 配置文件（导入即可复刻）。
- `README.md`: 项目介绍与使用说明。
## 🛠 如何复现
1. 在 Dify 环境中选择“导入 DSL 文件”。
2. 上传本仓库中的 `.yml` 文件。
3. 在节点设置中补全您的 API Key（OpenAI/DeepSeek）。
4. 关联相关的招生政策知识库 PDF 即可运行。
5.![工作流全景图](./workflow-all.png)  
