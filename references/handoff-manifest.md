# 上游交接清单

从对话、文件和 `packaging-cmf-finishes` 的交付结果中提取。只有关键缺失会导致物理错误或幻觉时才询问用户。

```yaml
project:
  name: ""
  category: ""
  use_case: "portfolio | proposal | ecommerce | social"

canonical:
  hero_render: "绝对路径"
  approved: true
  source_artwork: []
  panel_images: []
  other_approved_views: []

physical:
  package_type: "box | bottle | pouch | can | jar | other"
  structure: ""
  dimensions_mm: ""
  material: ""
  finishes: []
  finish_regions: []

identity_lock:
  brand_name: ""
  logo_description: ""
  protected_text: []
  key_graphics: []
  primary_colors: []
  forbidden_changes: []

series:
  tier: "6 | 10 | 14"
  subseries_id: "portfolio-4x5"
  aspect_ratio: "4:5"
  orientation: "portrait | landscape"
  canvas_px: "pixel_width × pixel_height"
  primary_narrative: "cultural-icon | concept-mechanism | brand-system | sensory-craft | appetite-direct | material-responsible | oriental-lifestyle"
  secondary_narrative: "可空"
  background_direction: "clean light studio"
  art_direction_concept: ""
  palette_family: []
  lighting_motifs: []
  composition_motifs: []
  scale_ladder: "standard_front_percent | group_item_percent + group_envelope_percent | context_percent + negative_space_role | macro_crop_anchor"
  required_shots: []
  prohibited_props: []
  output_dir: "绝对路径"
```

## 硬阻断

- 没有已确认视觉母版：先回到 `packaging-cmf-finishes` 生成或确认主效果图。
- 没有物理尺寸：询问实际 mm 尺寸或让用户明确同意上游默认尺寸。
- 要展示未知背面/侧面/内衬但没有源纹理：请求平面稿、面板或已确认视图。
- 包装属于瓶装或软包装时，上游所需的瓶身/标签或袋型/封边信息同样必须齐全。

## 可安全默认

- 用途：作品集案例展示。
- 图数：标准 10 张。
- 画布：同一子系列锁定完全一致的像素宽高、画幅和方向；只记录 4:5 等比例不够。
- 画幅：4:5 竖版；必要时另建独立的 16:9 封面子系列，不与主系列混合验收。
- 摄影：纯净浅色影棚、柔光、克制阴影、大留白。
- 场景道具：最多 1–3 类，与产品真实使用情境直接相关。
