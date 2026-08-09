# Sober Love · 清醒恋爱

> **行为证据 ＞ 语言解释 ＞ 主观感受。**
> Actions speak. Words explain. Feelings just wish.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Online Demo](https://img.shields.io/badge/🌐_在线使用-Sober_Love-3b5bdb)](https://deno0521.github.io/sober-love/)
[![Zero Backend](https://img.shields.io/badge/backend-none-orange)](#)

**[🌐 点我直接使用（无需注册，数据不出浏览器）](https://deno0521.github.io/sober-love/)**

---

## 你有没有过这些时刻？

- 他说「最近很忙」——是真的忙，还是在降温？你分不清。
- 她说的每一句话都很动人，但你回头一想，好像什么都没发生过。
- 朋友问你「TA 对你好吗」，你说「挺好的」，但让你举三个例子，你卡住了。

**感觉会骗你，证据不会。**

Sober Love 是一个给关系「做体检」的小工具：回答 30 个可以用证据验证的是/否问题，它会告诉你——这段关系目前**值不值得继续投入、最大的风险在哪、下一步具体该做什么**。

不安慰你，不替你找借口，不评价好人坏人。只处理证据。

---

## 3 分钟上手

1. 打开 [在线工具](https://deno0521.github.io/sober-love/)
2. 每个维度回答 5 个证据问题（例：「过去 30 天，TA 的明确承诺兑现率 ≥ 2/3？」），自动生成参考分
3. 得到你的专属报告：**关系可靠度 R 值 + 一句话结论 + 行动方案 + 验证任务**
4. 可勾选模块导出 PDF，30 天后对照重新评估

## 它会给你什么

- 🎯 **一句话结论**（五选一，绝不模棱两可）：值得继续发展 / 控制速度 / 停止加码观察 / 高风险暂停 / 核心信任已破坏
- 📊 **关系可靠度 R 值**：加权模型，完整展示计算过程
- 🧱 **结构性风险警报**：总分 70 但信任只有 20？模型不许你用平均分骗自己
- ⚠️ **三大危险指标排序**：只解释为什么重要，不替 TA 找理由
- 🔍 **假性高分检测**：「对我很好但现实身份长期隐藏」这类虚高组合会被自动揪出来
- 🚩 **硬性红旗优先**：已确认的重大欺骗、隐瞒伴侣、操控、威胁暴力——直接否决，不允许稀释
- ✅ **下一阶段验证任务**：全部基于正常真实互动，不试探、不钓鱼、不查手机
- 📄 **选择性 PDF 导出**：报告里放什么，你自己勾

## 为什么打分不会"凭感觉"？

传统打分最大的敌人是自己的主观偏差。Sober Love 用**三层锚定**对抗它：

1. **档位锚点**——每一档都对应具体行为描述，打分必须对号入座
2. **证据底线**——每项 5 个可验证的证据问题，算出一个"证据能支撑的分数"
3. **偏差警报**——你的输入偏离证据参考值 ±15 分即亮红牌，并同时显示「你的 R」与「证据的 R」

工具不能消灭偏差，但能让偏差无处藏身。

## 底层模型（给想较真的人）

六项参数加权：**R = 0.25·A行动 + 0.25·T信任 + 0.15·C连接 + 0.15·P互惠 + 0.10·S信噪比 + 0.10·(100−H不确定性)**

但总分从不是结论——结构性风险检查与硬性红旗机制拥有更高优先级。完整规则见 [模型文档](#)（页面内各模块均有说明）。

## 隐私

纯前端单文件，零后端、零追踪、零网络请求。你的数据只存在于你的浏览器里，关掉页面就没了——关系的细节，本来就不该上传给任何人。

## 本地运行 / 二次开发

```bash
git clone https://github.com/DENO0521/sober-love.git
cd sober-love
# 浏览器直接打开 index.html 即可，无需构建
```

整个项目只有一个 `index.html`（HTML + CSS + 原生 JS），欢迎 Fork 改成你的版本。

---

## English

**Sober Love** is a single-file web tool that scores your relationship with *evidence* instead of feelings.

**[🌐 Try it online](https://deno0521.github.io/sober-love/)** — no signup, no backend, your data never leaves your browser.

### Why

Feelings lie. Evidence doesn't. When you can't tell "he's genuinely busy" from "he's fading away", you need a framework that forces you to separate what *happened* from what you *hope*.

### How it works

1. Answer 30 yes/no evidence-based questions across 6 dimensions (Actions, Trust, Connection, Payoff, Signal-to-noise, Entropy)
2. Get a weighted reliability score **R (0–100)** with full calculation breakdown
3. Structural risk checks override the total — a 70 average can't hide a 20 in Trust
4. Confirmed dealbreakers (major lies, hidden partner, manipulation, threats) trigger an immediate stop recommendation — never diluted by averages
5. Receive one of four action strategies (Proceed / Slow down / Observe / Stop) plus up to 3 concrete verification tasks for the next 30 days
6. Selectively export modules to PDF for your records

### Anti-bias design

Three-layer anchoring keeps self-deception visible: behavioral anchors per score band → evidence-based reference scores → automatic drift alerts when your input deviates ±15 from what the evidence supports.

### Tech

Zero dependencies. Zero build step. One `index.html`. Fork it, remix it, make it yours.

---

## 免责声明 / Disclaimer

本工具是基于「行为证据优先」原则的决策辅助框架，输出仅反映你输入的证据，不构成心理咨询或情感咨询建议。任何关系决策的最终责任由使用者本人承担。
This tool is a decision-aid framework, not psychological or relationship advice. You own your decisions.

## License

MIT © [DENO0521](https://github.com/DENO0521) — 随便用，注明出处即可。
