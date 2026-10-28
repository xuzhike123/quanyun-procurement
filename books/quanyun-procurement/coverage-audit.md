# 覆盖审计：原文件关键任务 → 交付去向

审计对象为三份文件里"读者实际会来问的事"，不是章节标题。每一行都必须有明确去向，不允许静默消失。

| # | 原文件关键任务 | 出处 | 候选单元 | 判定 | 交付去向 |
|---|---|---|---|---|---|
| 1 | 判断一笔采购适不适用采购办法 | 60号 第二条、第三条 | 射程判定 | verified | cap.quanyun.scope-attribution |
| 2 | 判断工程与采购混装时走哪套制度 | 60号 第六条 | 占比判定 | verified | cap.quanyun.scope-attribution（50% 规则） |
| 3 | 判断哪些情形豁免适用 | 60号 第五十二条 | 六类例外 | verified | cap.quanyun.scope-attribution |
| 4 | 找归口管理部室 | 60号 附件1 | 归口对照 | verified | cap.quanyun.scope-attribution + `resources/department-attribution.md` |
| 5 | 判断金额档位 | 60号 第五条、第七条 | 档位与口径 | verified | cap.quanyun.approval-route |
| 6 | 确定审批链 | 60号 第二十二条、附件2 | 审批矩阵 | verified | cap.quanyun.approval-route + `resources/approval-matrix.csv` |
| 7 | 预算外与超预算重新报批 | 60号 第二十条、第二十二条 | 重新报批规则 | verified | cap.quanyun.approval-route |
| 8 | 选择采购方式 | 60号 第二十六至二十九条 | 方式选择 | verified | cap.quanyun.procurement-method |
| 9 | 论证能否不公开招标 | 60号 第二十七条 | 邀请招标与单一来源情形 | verified | cap.quanyun.procurement-method |
| 10 | 流标后如何处理 | 60号 第二十八条 | 二次招标规则 | verified | cap.quanyun.procurement-method |
| 11 | 已中标项目对外分包报批 | 60号 第二十四条 | 分包审批 | verified | cap.quanyun.procurement-method |
| 12 | 零星小额月度归集 | 60号 第二十五条 | 归集流程 | verified | cap.quanyun.minor-emergency |
| 13 | 应急采购先实施后补件 | 60号 第二十五条第四项 | 补件时限 | verified | cap.quanyun.minor-emergency |
| 14 | 内部采购定价 | 60号 第三十二、三十三条、附件8 | 比率表 | verified | cap.quanyun.internal-pricing |
| 15 | 台账编制与季度报送 | 60号 第四十一条 | 报送节奏 | verified | cap.quanyun.archive-reporting |
| 16 | 年度执行情况报送 | 60号 第五十一条 | 年度节点 | verified | cap.quanyun.archive-reporting |
| 17 | 归档材料清单 | 60号 第四十条 | 归档清单 | verified | cap.quanyun.archive-reporting |
| 18 | 三重一大事项该上哪个会 | 78号 第四至七条 | 主体归属 | verified | cap.quanyun.szyd-routing |
| 19 | 会议怎么开、怎么表决、怎么记录 | 78号 第八至十一条 | 决策程序 | verified | cap.quanyun.szyd-procedure |
| 20 | 紧急临时决策与追认 | 78号 第十二条 | 特殊通道 | verified | cap.quanyun.szyd-procedure |
| 21 | 决策后能否变更、如何变更 | 78号 第十四条 | 执行与变更 | verified | cap.quanyun.szyd-procedure |
| 22 | 月度报告与零报告 | 78号 第十三条 | 报告制度 | verified | cap.quanyun.szyd-procedure（archive-reporting 提示不可互替） |
| 23 | 监督主体与分工 | 78号 第十六至十八条、60号 第四十二至四十三条 | 监督三条线 | verified | cap.quanyun.compliance-redline |
| 24 | 采购人员禁止行为 | 60号 第四十五条 | 七项红线 | verified | cap.quanyun.compliance-redline |
| 25 | 供应商违规处理 | 60号 第四十八条 | 黑名单 | verified | cap.quanyun.compliance-redline |
| 26 | 决策失误责任划分与免责 | 78号 第十九条 | 责任规则 | verified | cap.quanyun.compliance-redline |
| 27 | 采购原则（六条） | 60号 第九至十四条 | 原则表述 | reference | `book/overview.md` 第三节、`book/glossary.md` |
| 28 | 保障体系（制度/内控/信息/合同/质量） | 60号 第三十五至三十九条 | 条款要求 | reference | 拆入 cap.quanyun.compliance-redline 的执行步骤 |
| 29 | 集中采购与信创电脑采购 | 60号 第三十三、三十四条 | 指引条款 | reference | 写入 internal-pricing 与 scope-attribution 的边界 |
| 30 | 供应商评价与黑名单管理办法 | 60号 第十四条（指向闽泉运综合〔2026〕33号） | 外部文件 | needs_review | 见 needs-review.md，材料未提供原文 |
| 31 | 工程建设相关采购 | 60号 第三条 | 排除项 | reference | out_of_scope 与各卡边界 |
| 32 | 上交集团层面的审批规则 | 62号 第十三至十六条 | 上位规则 | verified | 并入 cap.quanyun.approval-route（注明适用主体为交发集团本部） |

## 结论

原文件 32 项关键任务全部有明确去向，其中 25 项编译为 active 能力、6 项作为 reference 并入 overview/glossary 或边界说明、1 项标记 needs_review（依赖未提供的外部文件）。无未解释遗漏。
