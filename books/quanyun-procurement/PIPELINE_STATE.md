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
