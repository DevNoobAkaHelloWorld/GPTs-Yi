# GPTs-Yi

> Quantum-Driven I Ching Divination with Observer-Entangled Randomness

## 项目简介

**GPTs-Yi** 是一个结合了 GPT 智能体、量子随机数（Quantum RNG）、知识检索（RAG）与《易经》哲理的现代占卜系统。我们尝试回答一个古老而现代的问题：

> “当你点击一个按钮请求卦象时，你的意念是否真的能影响结果？”

本项目基于 **澳大利亚国立大学（ANU）的量子随机数平台** 作为起卦的底层随机源，以模拟“以心感应”的起卦机制。卦象生成后，我们通过 **GPTs + 本地《易经》语料库（十翼、彖传、象传等）+ RAG 检索机制**，为每一卦象生成个性化的占解与指引。

### 特点亮点

- 🧠 **以心感应、量子干预**：用户的“点击行为”被视为对量子态的观测，从而触发波函数坍缩，生成卦象。此过程在哲学上模拟“观者即参与者”的宇宙观。
- 📚 **嵌入式《易经》知识系统**：将《易经》全书（含十翼）转化为结构化 JSON 并接入 GPT 的知识检索链条，确保解释有据可循。
- 🔮 **非微调式智能增强**：本系统未修改 GPT 模型本身参数，而是通过 Prompt 编排、RAG、外部动作等组合机制进行个性化响应，具备良好的通用性与可移植性。
- 🧩 **可拓展的 Agent 架构**：支持未来接入语音起卦、图像反馈、动作生成等多模态扩展。

## 起卦机制（Quantum Casting Mechanism）

我们使用 ANU 的 Quantum Random Number Generator 接口获取三组六位二进制数据，对应易经六爻起卦流程：

- 每次用户点击“起卦”，将请求一组量子随机数（或使用 GPT 模拟调用）；
- 同时记录时间戳、用户输入、意图（可选）作为观察者信息；
- 六个数字决定爻象，最终生成卦象（初爻至上爻）；
- 若有变爻，自动生成本卦、之卦与互卦，并进行解释。

## 系统架构

```
[User Interface]
      ↓
[Quantum RNG API] ←— User Trigger (Observer Effect)
      ↓
[Hexagram Generator]
      ↓
[Prompt + RAG Retriever] ←— Yi Corpus (JSON of Ten Wings, Hexagram Text)
      ↓
[GPT Inference] → Formatted Explanation + Philosophical Commentary
```
## 灵感来源

- 《易经·系辞传》：“心物感应、阴阳互动”
- Everett 多世界理论与波函数坍缩
- GPT + RAG 构建“语义解释器”体系

## 项目状态

本项目目前为 **实验性哲学交互系统**，欢迎 PR / Fork / 哲学批判。

## License

MIT License. 卦象无主，人人皆可参天。
