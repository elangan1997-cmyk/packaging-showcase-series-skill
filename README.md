# 包装作品集图组 Skill

> 把单张包装工艺效果图延展为统一、连贯、作品集级的产品展示图组

## 一句话说清楚

有了 `packaging-cmf-finishes` 生成的主效果图之后，这个 Skill 自动把它延展成一整套 6/10/14 张的产品展示图组——有封面、有结构、有微距、有场景、有系列感，直接可以发 Behance 或给客户提案。

## 和 packaging-cmf-finishes 的关系

```
packaging-cmf-finishes          packaging-showcase-series
      ↓                                ↓
 单张主效果图          →          整套作品集图组
 (1张确认稿)                     (6/10/14张系列)
```

上游 Skill 确认的主效果图是本 Skill 的「视觉母版」——所有延展图的结构、颜色、材质、文字、工艺都以此为基准，不会重新设计包装。

## 三档系列规格

| 档位 | 张数 | 适用场景 |
|---|---|---|
| 精简 | 6 张 | 快速提案、内部评审 |
| 标准（默认） | 10 张 | 完整 Behance 案例、品牌提案 |
| 完整 | 14 张 | 品牌发布、电商详情全案 |

## 10 张标准系列的镜头节奏

```
01_hero      → 叙事封面/视觉锚点（极近裁切或小主体大环境）
02_front     → 看清产品/标准视图（理性正视中轴）
03_group     → 组合陈列/多产品集群
04_structure → 结构/开合/盒型展示
05_finish    → 工艺微距（烫金/UV/击凸细节）
06_detail    → 材质微距/纹理
07_context   → 使用场景/生活方式
08_series    → 系列 SKU/色彩变体
09_flatlay   → 组件平铺/内容物
10_ender     → 收尾/记忆点
```

## 工作流程

```
视觉母版 + 物理数据 + 平面稿
  → 1. 锁定视觉 DNA（结构/文字/色彩/工艺/摄影语言）
  → 2. 建立概念发动机 + 艺术指导卡
  → 3. 制定镜头表（每张有独立任务，不换背景凑数）
  → 4. 锁定画布契约（同系列每张像素一致）
  → 5. 逐张生成 → 单张 QA 验收 → 不通过就重做
  → 6. 系列终检（组图放在一起像同一项目）
  → 7. 交付
```

## 核心约束

- **包装不变**：结构、尺寸、Logo、文字、色彩、材质、工艺前后一致
- **不虚构内容**：背面/侧面/内衬没有原始纹理就不生成
- **每张有独立任务**：两张相邻图片至少改变 4 项构图指标
- **不凑数量**：只换背景、色温或角度不算新镜头
- **纯 AI 生成**：禁止本地代码合成、修图、换文字
- **物理尺寸必填**：没有 mm 尺寸就停下来问

## 禁止的陈词滥调

花瓣、丝绸、水滴、烟雾、石材、金属球、每张都 45° 角、无意义空白冒充高级感

## 安装

### Claude Code
```bash
git clone https://github.com/elangan1997-cmyk/packaging-showcase-series-skill.git \
  ~/.claude/skills/packaging-showcase-series
```

### Codex CLI
```bash
git clone https://github.com/elangan1997-cmyk/packaging-showcase-series-skill.git \
  ~/.codex/skills/packaging-showcase-series
```

## 使用方式

```
帮我把这个效果图延展成一套 10 张的作品集图组
```

或指定用途：

```
做一套 Behance 包装案例，标准 10 张，4:5 竖版
```

## 触发关键词

继续延展一整套包装展示图、做 Behance 包装案例图、生成多角度组合陈列开盒工艺微距使用场景系列 SKU、作品集长图素材

## 依赖

- `packaging-cmf-finishes` Skill（上游，提供主效果图和物理数据）
- AI 图像生成模型（图生图）

## 输出

- 系列图片（项目名_01_hero_v1.png 等）
- 镜头清单（shot-manifest.md）

## 许可

MIT
