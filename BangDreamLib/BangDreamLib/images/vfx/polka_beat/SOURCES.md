# 波点律动特效素材来源

素材由 Polaris 资产库（`D:\PolarisAssets`）导出后重命名。库中的数字名对项目无意义，
此表用于日后换素材时反查来源。网格参数取自 `get_asset_group_preview`，不要目测。

| 项目内文件 | 库资产名 | 资产 uuid | 字节 | 尺寸 / 网格 | 用途 |
|---|---|---|---|---|---|
| `polka_beat_dots.png` | `zumama_72_103_angel` | `09d7dafb-47f6-440a-bb95-12d1db95fe24` | 58928 | 256×256 单帧 | 波点律动着色器的网点遮罩（取其 alpha 作浓度） |
| `polka_beat_ring_sheet.png` | `fx_311900_tex_007` | `2206e367-6232-431c-a12b-3bc5986e0d27` | 27289 | 3×3，单帧 85×85（`hframes=3 vframes=3`） | 命中扩散环序列帧 |
| `polka_beat_shock_ring.png` | `airbomb_01` | `595e4697-0cda-4458-a240-01803041861f` | 2335 | 64×64 单帧 | 命中冲击波环 |
| `polka_beat_core_flash.png` | `305600_skill0_core_ex` | `cb44d5d6-6324-4920-8700-844bc8c720d4` | 6861 | 124×124 单帧（黑底，加法混合） | 命中闪光主层 |
| `polka_beat_stars.png` | `star_235` | `cb1dcef0-300d-45ba-a0c4-9b3a299a06ba` | 20105 | 2×2，单帧 64×64（`hframes=2 vframes=2`） | 星点粒子（蓝/金/紫/青四款） |

波点精灵（波点环、波形带、律动核、波点粒子）与加法混合材质**不另存副本**，
直接用仓库已有的游戏资源：

| 资源 | 用途 |
|---|---|
| `res://images/vfx/dot.png`（uid `uid://d2srbops1xqm0`，256×256 柔和白点） | 波点环 / 波点波形带 / 律动核 / 波点粒子 |
| `res://images/vfx/vfx_confetti/spark.tres`（uid `uid://cla2wesmc11oy`，`blend_mode=1`） | 各精灵的加法混合材质 |

> 曾试过用 `special_object_angel2_01`（金白音波条）与 `special_object_angel2_#6_08`（金色谱号装饰）
> 做节奏点缀，但金橙色与主题色冲突、硬剪影像「盖章」，已换成上述纯波点实现并从目录移除；
> `oblvns_skin_05`（音符图集）也曾作为音符粒子使用，因与波点语言重复而一并移除。

`.import` 文件必须随 PNG 一起提交，否则他人拉取后需要重新导入才能打开场景。