# PIPELINE_STATE

- 内容：《福建省泉运实业集团有限公司物资采购及购买服务管理办法》（闽泉运综合〔2026〕60号，含附件1–8）、《泉州交通发展集团有限责任公司关于印发〈集团物资采购及购买服务管理办法〉的通知》（泉交发〔2026〕62号）、《中共福建省泉运实业集团有限公司委员会关于修订印发〈"三重一大"决策制度实施办法〉的通知》（闽泉运党委〔2026〕78号，含附件报告表）
- 文本来源：用户上传的三个本地文件，docx 经 OOXML 解析提取，doc 经本机 Word 转换后转码提取
- 工具链：cangjie-skill v2.5.0，`scripts/cangjie.py doctor` PASS
- 输出模式：single（用户未指定，按 single-first 原则）
- 当前阶段：阶段 5 已完成，产物已编译并发布

## 阶段记录

| 阶段 | 状态 | 产出 |
|---|---|---|
| 0 整书理解 | 完成 | `book/overview.md` |
| 1 并行提取 | 完成（串行执行，环境未起 sub-agent） | `candidates/` 归并进各能力卡 |
| 1.5 三重验证 | 完成 | `verified.md` |
| 1.6 晋级门 | 完成 | 9 张卡全部 destination=router，见 `verified.yaml` |
| 2 RIA++ 构造 | 完成 | `cards/*.md` 共 9 张 |
| 3 Zettelkasten | 完成 | 各卡 `also_read` + `book/glossary.md` |
| 4 压力测试 | 部分完成 | 见 `verified.md` 评测用例一节 |
| 5 编译交付 | 完成 | 仓库根目录 `SKILL.md` + `references/` + `resources/` |

## 断点续跑提示

若需修订内容，改 `books/quanyun-procurement/.cangjie/capabilities/` 下的 `verified.yaml` 与 `cards/`，再运行：

```
python scripts/cangjie.py compile \
  --bundle books/quanyun-procurement/.cangjie/capabilities \
  --out <目标目录> --output single --yes
```

不要直接手改编译产物，否则下次编译会被判定为本地手改并拒绝覆盖。

## v1.1.0 增量更新（2026-11-03，流水线外）

新增素材：泉交发〔2026〕244号《招标文件联合会审实施细则》（交发集团，2026-10-20 印发，集团 2026 年第 13 次总经理办公会议通过；全文提取件存工作区 `_src/d4.txt`）。

本次为**增量更新**，编译产物（仓库根目录）直接同步自安装版 `~/.workbuddy/skills/qycg-skill` v1.1.0：

- 新增第 10 张能力卡 `tender-joint-review.md`（招标文件联合会审：门槛 / 八步流程 / 责任链 / 配套材料 / 一次审结 / 5 个工作日 OA 备案）；
- `SKILL.md`：路由表新增一行、核心原则新增第 8 条、description 触发词扩充、capability-count 9→10；
- `overview.md` / `glossary.md` / `cheatsheet.md` / `capability-index.md` 同步扩充；
- `procurement-method.md` / `scope-attribution.md` 增加与联合会审卡的交叉引用；
- `references/` 卡片由 `references/capabilities/` 三级结构扁平化为两级（与开放平台上传包一致）；
- `BUILD_MANIFEST.json` 哈希全量重算。

**注意**：`books/quanyun-procurement/.cangjie/capabilities/` 下的 bundle（verified.yaml + cards/）仍为 v1.0 状态，未补录第 10 项能力。下次全量重编译前，需先将 `tender-joint-review` 按既有条目格式补录进 `verified.yaml`（含 intents / keywords / also_read），否则流水线会忽略该卡。

技能名变更：v1.1 起技能 `name` 统一为 `qycg-skill`（避免与历史安装副本触发词冲突），bundle-id 保留 `bundle.quanyun-procurement`。

## v1.2.0 条文复核修正（2026-11-06，流水线外）

触发：撰写《55万汽车租赁服务采购全流程与依据.md》时回查 `_src/d1.txt`、`_src/d2.txt` 原文，发现此前漏读了一句决定性条款。

**复核事实**：闽泉运综合〔2026〕60号 第二十二条（二）1 末句为"如集团'三重一大'决策制度实施办法对于采购项目金额另有规定的，从其规定"（`_src/d2.txt` 第 78 行）；闽泉运党委〔2026〕78号 第六条 1（4）把"50 万元（不含）以上的单项或批量大宗物资采购及购买服务及其采购方式的确定"列为董事会审议事项（`_src/d1.txt` 第 112 行）。二者构成转致适用，v1.0/v1.1 记为"条文冲突、停下交人工确认"属误判。

**本次修订范围**（编译产物与流水线事实源同步，避免下次重编译回退）：

- 编译产物：`SKILL.md`（version 1.0.0→1.2.0、description 增转致规则、核心原则新增第 9 条、边界与判停改写）、`references/szyd-routing.md`（相邻能力区分 + B 段）、`references/overview.md`（批判性阅读第一处）、`references/approval-route.md`、`references/cheatsheet.md`、`references/glossary.md`。
- bundle：`verified.yaml`（core_principles 补第 8/9 条、stop_conditions 改写）、`cards/szyd-routing.md`（整卡同步）、`cards/approval-route.md`、`book/overview.md`、`book/glossary.md`。
- 审计轨迹：`needs-review.md` 第 1 节改写为"已消解"并保留原记录、`verified.md` needs_review 段与压力测试 T5 期望输出修正、`DIGEST.md` 第七节改写、`README.md` 版本记录/已知问题/目录结构/生成方式、`PIPELINE_STATE.md` 本节。
- `BUILD_MANIFEST.json` published_hashes 全量重算；`dist/qycg-skill.zip` 重建。

**仍未同步项（下次全量重编译前必须处理）**：bundle 的 `capabilities` 列表仍为 9 项，未补录 `tender-joint-review`；`entry.name` 仍为 `quanyun-procurement`（编译产物为 `qycg-skill`）；`entry.description` 未补 244号 与转致规则相关触发词。若直接重编译，会丢失第 10 张卡并把技能名改回旧值，须先按既有条目格式补录后再编译。

**遗留不确定项**：采购办法中的"集团领导会议"是否即"总经理办公会"，以及董事会审议与采购领导小组专题会的先后顺序，四份文件均未定义。v1.2 的处理是两套会议并存留痕、涉及排期提示核对集团现行做法，不自行删减环节。
