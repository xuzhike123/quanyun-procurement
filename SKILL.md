---
name: quanyun-procurement
description: |
  当用户要判断泉运集团（福建省泉运实业集团有限公司）及其权属企业的采购该怎么走流程、该谁批、该用哪种采购方式，或者要判断某事项属于党委会/董事会/总经理办公会哪一主体决策时调用。覆盖：制度射程与归口部室、金额分档与审批链（1万/20万/50万/200万/500万/1000万/2000万）、公开招标与邀请招标及单一来源例外、流标二次招标、零星小额月度归集与应急采购补手续、内部采购定价标准、台账备案与季度年度报送、三重一大议事主体归属与六步决策程序、廉洁红线与责任追究。不适用于工程建设项目招投标、法律意见与审计结论出具。Triggers: 泉运集团/交发集团/采购审批/采购方式/限额以上/限额以下/零星小额/内部采购/三重一大/党委前置研究/董事会审议/总经理办公会/归口部室/采购会签单/阳光采购平台
metadata:
  cangjie.generated-by: cangjie-tools v2.5.0
  cangjie.variant: single
  cangjie.bundle-id: bundle.quanyun-procurement
  cangjie.capability-count: 9
  cangjie.entrypoint-count: 1
---
# 泉运集团非工程类采购与"三重一大"决策制度汇编 — 全书能力入口

## 触发与不触发

**适用**：与本书能力域相关的咨询与任务（见下方路由表的意图列）。
**不适用**：
- 工程建设项目招投标，包括工程施工以及与工程建设有关的货物和服务，按工程管理制度执行。
- 出具法律意见书、审计结论、税务处理方案。
- 代替企业作出实际决策，或代替审批人签署文件。
- 判断某供应商报价是否合理，此类判断需要市场行情数据支撑。

## 核心原则（常驻速览，概览类问题读到这里即可回答）

1. 先判射程再谈流程。工程建设项目、使用工会经费等非行政支出的限额以下采购、商业流通与品牌代理采购都不在这套办法的射程内，射程判错后面每一步都错。
2. 金额是唯一硬开关。先算单项或批量估算价，再按 20 万、50 万、200 万三个台阶决定走会签单、采购领导小组会还是报上级审批。
3. 审批权不下放。限额以下采购统一由泉运集团审批，权属企业没有审批决策权；限额以上统一由交发集团审批。
4. 归口决定谁签字。先按采购标的找到归口管理部室，再谈流程，否则会签单无人可批。
5. 决策与执行分离。需求、询价、定价、采购、验收、结算必须分岗分设，任何一人到底的安排都不合规。
6. 三重一大看事项类型而非金额。同一笔支出归党委会、董事会还是总经理办公会，由事项性质决定；党委会只做前置研究，不做前置决定。
7. 留痕即合规。会议纪要、会签单、台账、备案表、验收单缺一项，事后追责时企业无法自证。

## 能力路由（先读本表，按意图加载 1 张能力卡）

| 用户意图 | 先读 | 补读/备注 |
|---|---|---|
| 这笔采购适不适用采购办法；该找哪个部室归口；工程和采购混在一起怎么分 | references/capabilities/scope-attribution.md | references/capabilities/approval-route.md、references/capabilities/procurement-method.md |
| 这笔采购该谁审批；要不要上会，上哪个会；预算外和超预算怎么重新报批 | references/capabilities/approval-route.md | references/capabilities/scope-attribution.md、references/capabilities/szyd-routing.md、references/capabilities/archive-reporting.md |
| 这个项目能不能不公开招标；邀请招标要满足什么条件；流标了怎么办；采购方式怎么选 | references/capabilities/procurement-method.md | references/capabilities/approval-route.md、references/capabilities/scope-attribution.md |
| 零星小额怎么报；急事来不及审批怎么办；能不能先采购后补手续 | references/capabilities/minor-emergency.md | references/capabilities/approval-route.md、references/capabilities/compliance-redline.md |
| 内部采购定价怎么定；上浮下浮比例是多少；旅游包车内部结算价 | references/capabilities/internal-pricing.md | references/capabilities/procurement-method.md、references/capabilities/compliance-redline.md |
| 台账什么时候报；备案表怎么填；年度执行情况什么时候交 | references/capabilities/archive-reporting.md | references/capabilities/approval-route.md、references/capabilities/compliance-redline.md |
| 这事该上党委会还是董事会；多少金额要上董事会；党委前置研究怎么用 | references/capabilities/szyd-routing.md | references/capabilities/szyd-procedure.md、references/capabilities/approval-route.md |
| 三重一大会议怎么开；会上怎么表决；紧急情况能不能先定后报；决策后能不能改 | references/capabilities/szyd-procedure.md | references/capabilities/szyd-routing.md、references/capabilities/compliance-redline.md |
| 采购人员不能做什么；供应商违规怎么处理；决策失误怎么追责 | references/capabilities/compliance-redline.md | references/capabilities/szyd-procedure.md、references/capabilities/minor-emergency.md |

**非能力类查询**：
- 书名/作者/章节/整书概览 → references/overview.md
- 术语解释 → references/glossary.md
- 决策规则速查（不需要原文依据时） → references/cheatsheet.md
- 完整意图与关键词索引（本表未覆盖的意图先查这里） → references/capability-index.md

## 加载规则

- 每次任务先读本文件，再按路由表加载 **1** 张能力卡；任务明确跨域时最多加载 2 张。
- 概览/书名类问题不加载能力卡，用「核心原则」与 overview.md 回答。
- 路由表与 capability-index.md 都无法命中的意图，明确告知超出本书范围，不要硬套。

## 边界与判停

- 三份制度对同一事项给出不同审批主体时（例如 50 万元以上物资采购究竟归董事会还是总经理办公会），停止自行取舍，列出冲突条文交人工确认。
- 采购金额、采购类型或是否预算内无法确定时，先索要数据，不猜测档位。
- 涉及具体人员的责任认定、纪律处分定性，只提供制度依据，不作定性结论。
