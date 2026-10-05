# PUBLIC ASSET REVIEW — 参考图库公开上传审查

**当前审查对象（R9 · 2026-10-05）**：ABC 用户版包内 A / B 模块 `reference-library/` 全部 **47 张**图片（A 10 张、B 37 张）＋ 全部文本文件。
**审查方法**：逐图缩略全览（联系表）→ 含人物 / 标识疑点图全分辨率复核 → EXIF / 元数据检查 → 文本敏感信息模式扫描 → 与上一版公开树按 SHA-256 全量对比。
**结论（R9）**：**45 张随公开仓库发布；2 张移出**（未删除，保留于本地 `private-assets-review/`，已加入 `.gitignore`，不随仓库上传）。

## 一、R9 公开树：已移出（不随公开仓库上传）

| 文件 | 原因 |
|---|---|
| `B-photo-zine-v5.4.0/reference-library/positive/28_On_the_Hill.webp` | 画面含一名正对镜头、面部可辨的真人（游客人群中的一人），存在肖像 / 隐私风险 |
| `B-photo-zine-v5.4.0/reference-library/positive/14_Mutianyu_Second_World.webp` | 含 UNESCO「世界文化遗产」、AAAAA 等第三方官方标识元素；石碑照片来源无法核实 |

> 处理方式：移动、未删除。两张图与 R8 公开审查时移出的文件**字节完全一致**（SHA-256 `62f2349f…`、`fb489059…`），沿用同一处理结论，本次未新增审查项。
> 若确认可公开（如 28 号实为 AI 合成形象、14 号为本人拍摄），可随时移回原目录并同步更新本文件。

## 二、R9 增量核对（相对 R8 公开树）

- **新增图片：0 张。变更图片：0 张。**（全部 45 张公开图与 R8 公开树逐字节一致，无需重复审查）
- 唯一差异：`37_Wall_and_Heaven_approved.webp` 不在本次用户版包内，因此**本版公开树不再包含该图**；文件未被删除，仍完整保留在 git 历史中（R8 提交 `f7ccca4` / `35dee4e`），需要时可取回。

## 三、保留但已标注（含小尺寸 / 远景人物，无清晰可辨人脸）

- A `02_bridge_realistic_approved`：桥上人群为远景剪影
- A `05_tree_avenue_people_semantic_approved`：约 20–25 人，均为背影 / 远景（技能「语义保留人物」的示例图）
- A `03_full_scene_repaint`（cautionary）：失败案例中的远景小人
- B `05_Afterlight` / `10_Rush_Hour` / `12_Canal_Rhythm` / `13_Way_Home` / `15_Wall_Walk` / `21_Along_the_Ridge` / `30_Evening_Crossing`：小尺寸或远景人物

以上未发现可辨认正脸，判定为可公开。

## 四、已核查项（全库）

- 无私人 / 家庭 / 室内生活类照片；未发现可识别正脸（已移出的 1 张除外）
- 无证件、姓名、电话、车牌等敏感文字；图内文字均为设计标题 / 文案
- 未见第三方水印或来源平台标识
- 全部图片无 EXIF / XMP 元数据（无法由文件反推设备、时间、地点）
- 文本扫描（72 个文本文件全量）：未发现 API key、Token、密码、.env、本地绝对路径（`C:\` / `D:\` / 用户名）、聊天记录或缓存目录

## 五、低风险备注（保留，供确认）

- `19_High_Contrast_BW`、`16_Oil_Painted_Mountain`、`17_Retro_Halftone_Travel_Poster`：风格化 / 摄影感较强，未能确认绝对出处；如有版权顾虑可一并移出。
- 如你知道某些图源自网络素材或教程截图（不在上述清单内），请指出，我们将一并处理。

## 六、历史记录（R8 · 2026-10-03，保留备查）

当时审查对象为 A / B 模块 48 张（A 10、B 38）＋ `golden-backup/` ＋全部文本文件；结论为 46 张发布、2 张移出（即上表两张，路径当时为 `B-photo-zine-v5.3.4/…`）。

- `audits/PACKAGE_SHA256SUMS.txt` 与 `audits/*_MACHINE_QC.json` 为 R6–R8 历史档案，按当时的图片数量记录；与本公开树不一致属预期，不代表当前清单。
- `qc/` 下的清单按**当前公开树**生成；`qc/VALIDATION.json`、`qc/BUILD_EVIDENCE.json` 为完整包（47 张）的构建证据，按原字节保留，其计数与本公开树相差 2 张属预期。

## 七、待确认

1. 28 号、14 号是否移回？（默认：不移回，保持移出状态）
2. 低风险备注 3 张是否保留？（默认：保留）
3. `37_Wall_and_Heaven_approved.webp` 是否需要重新加入公开树？（默认：不加入，遵循本次交付包内容）
