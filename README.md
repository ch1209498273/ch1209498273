# 芦金宇 · AI 产品经理（大模型应用落地 · 评测与成本治理）

> 大多数 RAG 的问题不是答不出来，是答得太像真的。
> 规则确定性的事情，绝不下放给概率模型。

7 年 B 端复杂业务交付（通信 4 年 + 医疗 3 年）· 天津大学计算机硕士。
当前带领 4~6 人产研小组，面向 14 家血透中心、300+ 医护构建专科 AI 应用体系——出题 Agent、证据约束问答、成本对账，全部在生产环境日常运行。

## 两个正在跑的系统

**[keryo-training-showcase](https://github.com/ch1209498273/keryo-training-showcase)** · 血透医护培训考核平台
把 5 个模型工具砍成 2 个，把结构校验、引用比对、禁忌词、题型配比做成服务端四道确定性硬闸。引用落地率 136/136 逐字命中，单题模型调用降 35%，单题算力 ¥0.0016。[`eval/`](https://github.com/ch1209498273/keryo-training-showcase/blob/main/eval/README.md) 附四道硬闸的脱敏参考实现，一个带四类缺陷的批次会被逐闸拦下、整批降级。

**[medical-rag-assistant-showcase](https://github.com/ch1209498273/medical-rag-assistant-showcase)** · 证据约束医疗问答
指不回原文的必须拒答。三道闸门拦在答案出门之前，贯穿全部评测批次，内容错误答案发布 0 次。[`eval/`](https://github.com/ch1209498273/medical-rag-assistant-showcase/blob/main/eval/README.md) 附逐 claim 核验参考实现——里面故意放了一条数值幻觉和一条"半对"，可以亲眼看到它们被固定原因码拦下。

**其他**：[ds-animations](https://github.com/ch1209498273/ds-animations)（60 个交互动画讲数据结构，课堂实装） · [ai-lesson-prep](https://github.com/ch1209498273/ai-lesson-prep)（大学教师备课全流程 AI 技能包，MIT） · XiTing（ColorOS 息屏听剧工具）

## 我的产品判断

这些不是口号，每一条都在上面两个仓库里被代码兑现：

- **单一指标的提升如果伴随端到端下降，它不是提升，是把问题往下游推。**
- **工具不是越多越 Agent；动作空间越大，越难收敛、越难审计、越贵。**
- **用户永远不该看到"尚未验证"的答案。**
- 评测集先冻结再迭代；准入用值匹配，逐字匹配只做诊断——逐字口径会把"24 学时"和"二十四学时"判成两个答案。
- 一个不能被追问的数字，是负资产。

## 联系

📮 1209498273@qq.com ｜ 📍 武汉
正在看 AI 产品 / 大模型解决方案方向的机会，欢迎邮件联系。
