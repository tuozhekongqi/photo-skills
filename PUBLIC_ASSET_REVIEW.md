# PUBLIC ASSET REVIEW — 参考图库公开上传审查

**审查对象**：A / B 模块 `reference-library/` 全部 48 张图片（A 10 张、B 38 张）＋ `golden-backup/` 内容 ＋ 全部文本文件。
**审查方法**：逐图缩略全览（联系表）→ 含人物 / 标识疑点图全分辨率复核 → EXIF / 元数据检查 → 文本敏感信息模式扫描。
**结论**：**46 张随公开仓库发布；2 张移出**（未删除，保留于本地 `private-assets-review/`，已加入 `.gitignore`，不随仓库上传）。

## 一、已移出（不随公开仓库上传）

| 文件 | 原因 |
|---|---|
| `B-photo-zine-v5.3.4/reference-library/positive/28_On_the_Hill.webp` | 画面含一名正对镜头、面部可辨的真人（游客人群中的一人），存在肖像 / 隐私风险 |
| `B-photo-zine-v5.3.4/reference-library/positive/14_Mutianyu_Second_World.webp` | 含 UNESCO「世界文化遗产」、AAAAA 等第三方官方标识元素；石碑照片来源无法核实 |

> 处理方式：移动、未删除。若确认可公开（如 28 号实为 AI 合成形象、14 号为本人拍摄），可随时移回原目录。
> 注：`audits/PACKAGE_SHA256SUMS.txt` 与 `audits/*_MACHINE_QC.json` 仍按原始 48 张图记录（历史档案），与本公开树的 46 张不一致属预期。

## 二、保留但已标注（含小尺寸 / 远景人物，无清晰可辨人脸）

- A `02_bridge_realistic_approved`：桥上人群为远景剪影
- A `05_tree_avenue_people_semantic_approved`：约 20–25 人，均为背影 / 远景（技能「语义保留人物」的示例图）
- A `03_full_scene_repaint`（cautionary）：失败案例中的远景小人
- B `05_Afterlight` / `10_Rush_Hour` / `12_Canal_Rhythm` / `13_Way_Home` / `15_Wall_Walk` / `21_Along_the_Ridge` / `30_Evening_Crossing`：小尺寸或远景人物

以上未发现可辨认正脸，判定为可公开。

## 三、已核查项（全库）

- 无私人 / 家庭 / 室内生活类照片；未发现可识别正脸（已移出的 1 张除外）
- 无证件、姓名、电话、车牌等敏感文字；图内文字均为设计标题 / 文案
- 未见第三方水印或来源平台标识
- 全部图片无 EXIF / XMP 元数据（无法由文件反推设备、时间、地点）
- 文本扫描：未发现 API key、Token、密码、本地路径、账号等敏感信息

## 四、低风险备注（保留，供你确认）

- `19_High_Contrast_BW`、`16_Oil_Painted_Mountain`、`17_Retro_Halftone_Travel_Poster`：风格化 / 摄影感较强，未能确认绝对出处；如有版权顾虑可一并移出。
- 如你知道某些图源自网络素材或教程截图（不在上述清单内），请指出，我们将一并处理。

## 五、待确认

1. 28 号、14 号是否移回？（默认：不移回，保持移出状态）
2. 低风险备注 3 张是否保留？（默认：保留）
