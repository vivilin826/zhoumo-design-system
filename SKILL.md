---
name: zhoumo-design-system
description: 粥沫 Pinky 的视觉设计系统。用于图文卡片、公众号排版、HTML 页面，以及 PPT 的配色和人物风格统一；提供品牌色、角色规范、布局与模板。
license: CC BY-NC-SA 4.0
metadata:
  author: ESTHER不二 (esthersjw)
  repo: https://github.com/esthersjw/esther-design-system
  visual-brand: 粥沫 Pinky
---

> © 2026 ESTHER不二 (esthersjw) | CC BY-NC-SA 4.0
> 使用本 Skill 需署名原作者，禁止商用，修改后须以相同协议分享。

触发条件：当用户要求制作HTML网页、个人页面、教程页面、介绍型页面、landing page、活动页面、App型页面、作品集等任何前端设计相关任务时触发。也在用户说"做图文"、"图文卡片"、"小红书图文"、"文章转卡片"、"转成图文"、"做卡片"时触发。

## 保留原版设计，只适配品牌

用户于 2026-10-07 明确要求：以原版 Design Skill 和 Demo 为底，保留原版字体、排版、字号、间距、信息层级、布局与交互风格；只替换头像/角色、用户品牌署名和协调配色。不要因为替换 IP 重设计页面或改写为另一篇教程。原版滚动入场、导航、高亮、头像轨道等交互保留。此要求优先于其他文档中与原版风格冲突的泛化禁忌。

品牌界面三色：天空蓝 `#4E86C5`（原版主蓝标记）、蜜糖黄 `#F6C55F`（强调）、珊瑚红 `#F15A43`（点缀）；午夜蓝 `#183A70` 用于正文与深色结构，奶油白 `#FFF7E8` 作背景。字体继续用原版字体池，Pinky 角色固定色与造型保持一致。

## 粥沫 Pinky 默认配置

必读 `brand-dna.md`。后续 PPT、图文、公众号和页面默认使用粥沫 Pinky 色板与人物规范；不再询问已确认的品牌色和角色身份。布局与组件示例的旧配色服从品牌规范。生成角色插图时使用 `zhoumo-pink-ip-illustrations` 的标准图、样图与验收流程；本技能保存的标准图仅用于参考，不作为头像输出。默认头像使用用户指定的 `assets/pinky-avatar.png`；交付模板时将该文件复制到 HTML 对应的资源路径。制作 PPT 时结合演示文稿技能，本系统负责视觉规范。

## 使用方式（7步工作流）

### Step 1: 澄清需求
向用户确认5个问题：
1. **类型** — 教程/介绍/科普？活动页/Landing？App型/功能型？**图文卡片？** **公众号排版？**
2. **受众** — 给谁看的？技术水平？
3. **Section数** — 大概几屏内容？
4. **素材** — 有哪些文案/图片/数据？
5. **硬约束** — 必须包含什么？有没有合作品牌色？

### Step 2: 读规范
1. **必读** `brand-dna.md` — 确认品牌底层规范
2. 根据类型选读场景文件：
   - 教程型/介绍型/科普型 → `references/scene-tutorial.md`
   - 活动页/分享会/Landing → `references/scene-landing.md`
   - App型/功能型（看板/书架/Canvas） → `references/scene-app.md`
   - **图文卡片/小红书图文/文章转卡片** → `references/scene-cards.md`
   - **公众号排版/做分发** → `references/scene-wechat.md`

### Step 3: 拷模板
从 `assets/` 选择对应模板作为起点：
- 教程型 → `assets/template-tutorial.html`
- 活动页/Landing → `assets/template-landing.html`
- App型/功能型 → `assets/template-app.html`
- **图文卡片** → `assets/template-cards.html`

**从模板开始改，不从零写。**

### Step 4: 选布局组合
从 `references/layouts.md` 中选取 3~5 种布局模式，为每个 section 分配不同布局。

**每个 section 布局必须不同。**

（图文卡片模式：参考 `scene-cards.md` 中的推荐排版手法，为每页选择不同手法。）

### Step 5: 选组件填充
从 `references/components.md` 中选取组件填入各 section。

**硬规则：禁止使用任何HTML默认样式。** 所有引用块、列表、表格、卡片必须从 components.md 里选用对应组件的代码。不允许用默认 `<blockquote>`、默认 `border-left` 引用、无样式 `<ul>/<ol>`、默认 `<table>`。如果在 components.md 里找不到合适的，自己设计一个符合 brand-dna 规范的，但绝不能用浏览器默认样式。

### Step 6: 自检
对照 `references/checklist.md` 逐条检查：
- **P0 必须全过** — 任何一条不过就要改
- P1 应过 — 尽量满足
- P2 加分 — 锦上添花

（图文卡片模式：额外对照 `scene-cards.md` 底部的 Checklist；公众号模式：额外对照 `scene-wechat.md` 底部的 Checklist，逐项检查标题是否发生非语义断行或英文断词。）

### Step 7: 交付
输出最终 HTML 文件，确保可直接在浏览器打开。

## 场景类型速查

| 类型 | 场景文件 | 模板 |
|------|----------|------|
| 教程型/介绍型/科普型 | `references/scene-tutorial.md` | `assets/template-tutorial.html` |
| 活动页/分享会/Landing | `references/scene-landing.md` | `assets/template-landing.html` |
| App型/功能型 | `references/scene-app.md` | `assets/template-app.html` |
| 图文卡片/小红书图文 | `references/scene-cards.md` | `assets/template-cards.html` |
| 公众号排版 | `references/scene-wechat.md` | `assets/template-wechat.html` |

## 关键原则
- **从模板开始改，不从零写** — 模板已内置品牌变量和基础结构
- **每个 section 布局必须不同** — 避免单调重复，从 layouts.md 选不同模式
- **做完必须跑 checklist** — P0 全过才能交付

## 禁忌
严格遵守 `brand-dna.md` 的禁忌清单，不在此重复。核心底线：截图发 Twitter 不会被说"又是AI做的"。
