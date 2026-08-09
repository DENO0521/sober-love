# Sober Love · 清醒恋爱 × 及时止损测算器

> **行为证据 ＞ 语言解释 ＞ 主观感受。该止损时，不加仓。**
> Actions speak. Words explain. Feelings just wish. Cut your losses in time.

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

## 为什么做这个工具？

因为大多数关系建议都坏在同一个地方：**它们问的是你的感受，而不是对方的行为。**

「你觉得 TA 爱你吗？」——这个问题没有答案，只有情绪。而「过去 30 天，TA 的承诺兑现了几件？」有答案，可以验证，无法自欺欺人。

这个工具做的事，就是把后者系统化：

- **把模糊的不安翻译成可验证的问题**——"我觉得 TA 在疏远我" → "与关系早期相比，TA 的行动投入有没有明显下降？"
- **把单次事件放进时间轴**——一次暖心举动说明不了什么，90 天的投入曲线才说明问题
- **把「再给他一次机会」变成明确的验证任务**——机会不是不可以给，但要有期限、有指标、有退出线
- **把止损从情绪决定变成风控决定**——亏到止损线就执行，不讨价还价

它不是让你变得冷漠，而是让你在投入真心之前，先确认对方值得。

---

## 不废话，直接上公式——开锤！🔨

六个学科，六个公式，每个配一个真实算例。看不懂公式没关系——工具帮你把计算全做了；看得懂的话，欢迎来挑错。

### 1️⃣ 微积分：投入函数的断崖检测

$$f'(t) \gg 0,\qquad f''(t) \ll 0$$

> **算例**：认识前两周，TA 每天主动找你 3 小时（$f'(t)\gg0$，投入高速增长）；第三周降到隔天回一句；第五周只剩「嗯」「哈哈」。峰值很高，但二阶导早已转负——**断崖不是突然发生的，曲线在崩塌前就已经向下弯了。看斜率，不看峰值。**

### 2️⃣ 贝叶斯：一次实锤撒谎值多少钱

$$P(A\mid B)=\frac{P(B\mid A)\,P(A)}{P(B)}$$

> **算例**：A =「TA 可靠」，先验 $P(A)=0.8$。B =「被证实重大撒谎」。设可靠者出现此证据的概率 $P(B\mid A)=0.05$，不可靠者 $P(B\mid\neg A)=0.6$：
>
> $$P(B)=0.05\times0.8+0.6\times0.2=0.16 \;\Rightarrow\; P(A\mid B)=\frac{0.04}{0.16}=\mathbf{0.25}$$
>
> 一次实锤，信任从 80% 打到 25%。**「我选择相信 TA」不是善意，是拒绝更新后验。**

### 3️⃣ 图论：社交网络的跨群边数

$$\mathrm{Connectivity}(A,B)\approx 0$$

> **算例**：你和 TA 的亲友、同事各是一张网。交往 6 个月，跨群边数 = 0——没见过 TA 任何朋友/同事/家人，TA 也从不进入你的圈子。健康基准：稳定交往 3 个月应有 ≥2 条跨群边。**0 条边不是「慢热」，是隔离。**

### 4️⃣ 博弈论：你的累计收益是负的吗

$$\sum \mathrm{Payoff}_{\text{you}} < 0$$

> **算例**：记 90 天的账——主动联系 58:7，解决实际问题 6:0，情绪安抚 11:1。折算每轮收益累计 $\sum\mathrm{Payoff}_{\text{you}}\approx -41 < 0$。**负和博弈里继续加仓，只会扩大亏损。止损线不是绝情，是风控。**

### 5️⃣ 信息论：信噪比与熵

$$\mathrm{SNR}=\frac{\mathrm{Signal}}{\mathrm{Noise}}\to 0,\qquad \mathrm{Entropy}\to\infty$$

> **算例**：30 天里「我会/下次/以后」类语句 21 条（Noise），可验证的兑现行动 3 件（Signal）→ $\mathrm{SNR}\approx0.14\ll1$。回复间隔序列 {0.5h, 0.5h, 26h, 1h, 49h} → 高熵，完全不可预测。**话越密，信越假；越无常，越危险。**

### 6️⃣ 综合：终极可靠度公式

$$R=\frac{\int \mathrm{Action}(t)\,dt}{\mathrm{Noise}}\times\frac{\mathrm{Connectivity}}{\mathrm{Entropy}}$$

> **算例**：行动与连通做分子，噪声与熵做分母。工具将其落地为加权评分 $R = 0.25A+0.25T+0.15C+0.15P+0.10S+0.10(100-H)$。代入 A=45, T=35, C=30, P=55, S=30, H=70：
>
> $$R = 11.25+8.75+4.5+8.25+3+3 = \mathbf{38.75}$$
>
> 落入高风险区（35–49）→ 系统判定：**停止加码，进入观察期**。

> ⚠️ **诚实声明**：除贝叶斯定理、SNR 等基本形式外，这些是启发式观察框架，不是经过验证的心理学诊断工具。我们把公式改造成可验证的问题清单，而不是假装在算精确数值。完整推导、变量说明与 LaTeX 源码见 [THEORY.md](THEORY.md)。

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

上面六个公式是观察框架；工具内部实际运行的是它们的可计算落地版：

$$R = 0.25A + 0.25T + 0.15C + 0.15P + 0.10S + 0.10(100-H)$$

| 参数 | 对应学科 | 权重 | 检查什么 |
|------|---------|------|---------|
| A 行动持续度 | 微积分 · 投入函数 | 0.25 | 承诺是否长期兑现 |
| T 信任度 | 贝叶斯 · 后验更新 | 0.25 | 证据是否支持信任 |
| C 现实连接度 | 图论 · 跨群边 | 0.15 | 是否进入 TA 真实生活 |
| P 关系收益度 | 博弈论 · 累计收益 | 0.15 | 投入是否对等互惠 |
| S 信噪比 | 信息论 · SNR | 0.10 | 行动多还是话术多 |
| H 不确定性 | 信息论 · 熵 | 0.10（反向） | 行为是否可预测 |

**总分从不是结论**——结构性风险检查（T<40 诚信高风险、T&A 双低禁止快速发展等）与硬性红旗机制拥有更高优先级。完整推导与严谨性备注见 [THEORY.md](THEORY.md)。

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

**Sober Love** is a single-file web tool that scores your relationship with *evidence* instead of feelings — and tells you exactly when to cut your losses.

**[🌐 Try it online](https://deno0521.github.io/sober-love/)** — no signup, no backend, your data never leaves your browser.

### The moments it was built for

- They say "I've been busy lately" — genuinely busy, or quietly fading? You can't tell.
- Every word they say is moving, yet looking back, nothing actually *happened*.
- A friend asks "do they treat you well?" You say "sure" — then can't name three examples.

Feelings lie. Evidence doesn't.

### The six formulas (yes, real math)

Each dimension of your relationship is mapped to a classic model, with worked examples inside the tool:

| Dimension | Model | Question it answers |
|-----------|-------|--------------------|
| **A** Action consistency | Calculus — investment derivative $f'(t), f''(t)$ | Is the effort curve sustainable or a cliff? |
| **T** Trust | Bayes' theorem $P(A\mid B)$ | Does the *evidence* still justify belief? |
| **C** Real-world connection | Graph theory — connectivity | Are you inside their actual life? |
| **P** Payoff balance | Game theory — $\sum \text{Payoff}_{you}$ | Is this reciprocal or a negative-sum drain? |
| **S** Signal-to-noise | Information theory — SNR | Do actions outweigh words? |
| **H** Entropy | Information theory — entropy | Is their behavior predictable? |

Composite output: $R = 0.25A + 0.25T + 0.15C + 0.15P + 0.10S + 0.10(100-H)$ — with structural risk checks that override the average. Honest note: apart from Bayes and SNR basics, these are heuristic observation frameworks, not validated psychological diagnostics. We turn them into verifiable question checklists instead of pretending to compute exact truth. Full derivations & LaTeX in [THEORY.md](THEORY.md).

### What you get

1. **A one-line verdict** — five levels, no hedging: proceed / slow down / observe / pause / trust broken
2. **Reliability score R (0–100)** with the full calculation shown
3. **Structural risk alerts** — a 70 average can't hide a 20 in Trust
4. **Top-3 risk ranking** — why each matters, no excuses made for anyone
5. **Fake-high detection** — "treats me well but keeps their real life hidden" gets caught automatically
6. **Hard dealbreaker override** — confirmed major lies, hidden partners, manipulation, threats: immediate stop, never diluted by averages
7. **Up to 3 verification tasks** for the next 30 days — all through normal interaction; no snooping, no traps, no tests
8. **Selective PDF export** — your report, your choice of modules

### Anti-bias design

Scoring your own relationship is biased by definition. Three-layer anchoring keeps self-deception visible: **behavioral anchors** per score band → **evidence-based reference scores** from 30 yes/no questions → **automatic drift alerts** when your input deviates ±15 from what the evidence supports, with "your R" and "evidence R" shown side by side.

The tool can't eliminate bias. It makes bias impossible to hide.

### Privacy

Zero backend, zero tracking, zero network requests. Everything is computed in your browser and gone when you close the tab — the details of your relationship were never meant to be uploaded to anyone.

### Run locally / Remix

```bash
git clone https://github.com/DENO0521/sober-love.git
cd sober-love
# open index.html in any browser — no build step
```

Zero dependencies. One `index.html`. Fork it, remix it, make it yours.

---

## 免责声明 / Disclaimer

本工具是基于「行为证据优先」原则的决策辅助框架，输出仅反映你输入的证据，不构成心理咨询或情感咨询建议。任何关系决策的最终责任由使用者本人承担。
This tool is a decision-aid framework, not psychological or relationship advice. You own your decisions.

## License

MIT © [DENO0521](https://github.com/DENO0521) — 随便用，注明出处即可。
