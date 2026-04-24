# GPT-Image-2 完全教程

> 从零到一掌握 OpenAI 最新图像生成模型的全攻略
>
> 整合官方文档、社区最佳实践、200+ 精选提示词、覆盖 10 大应用场景

[![GPT-Image-2](https://img.shields.io/badge/Model-GPT--Image--2-blue?style=for-the-badge)](https://chatgpt.com)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](LICENSE)

---

## 📑 目录

- [简介](#简介)
- [核心能力](#核心能力)
- [使用入口](#使用入口)
- [两种模式](#两种模式)
- [提示词框架](#提示词框架)
- [提示词合集](#提示词合集)
- [高级技巧](#高级技巧)
- [API 使用指南](#api-使用指南)
- [CLI 工具](#cli-工具)
- [局限性](#局限性)
- [最佳实践](#最佳实践)
- [参考资源](#参考资源)

---

## 简介

2026 年 4 月 22 日，OpenAI 正式发布 **ChatGPT Images 2.0**（API 模型名 `gpt-image-2`）。

### 🚀 四大核心突破

根据社区实测，GPT Image 2 有四大"超能力"：

| 能力 | 说明 |
|------|------|
| **完美文字渲染** | 复杂文字（英语、西里尔字母、亚洲脚本）100%准确，不再有"AI胡言乱语" |
| **身份一致性** | 同一角色/视觉IP在不同场景和角度中保持一致 |
| **结构化设计** | 生成复杂信息图、爆炸图、多面板布局 |
| **艺术意图** | 高保真风格迁移，捕捉艺术运动的"灵魂"而非表面颜色 |

### 关键参数

| 特性 | 详情 |
|------|------|
| 知识截止 | 2025 年 12 月 |
| 宽高比 | 3:1 ~ 1:3 |
| 多语言 | 中文、日文、韩文、印地语等 |
| 入口 | ChatGPT / Codex / API |

---

## 核心能力

### 1. 文字渲染（质的飞跃）

文字渲染一直是 AI 图像模型最大的痛点。GPT-Image-2 在中文渲染上实现了质的突破：

- 可以**默写出师表**，绝大多数文字保持稳定
- 能生成完整的**中文报纸**、**数学试卷**
- 支持**红楼梦关系图**等复杂信息图表
- 从一张照片直接生成**完整的电商产品详情页**

> **关键提示：** 中文文字不再是「贴图感」，而是真正融入了视觉设计的骨架。

### 2. 世界知识（最强护城河）

这是 GPT-Image-2 与其他模型拉开差距最大的能力：

- 生成 YouTube 首页截图 — 正确的布局、按钮样式、图标位置
- 生成小红书/B 站个人主页 — 甚至会自动编造完整的人设
- 游戏代肝海报 — 自动补充专业文案
- 汽车官网 — 仅凭一张车辆照片就生成完整的品牌官网

### 3. 修改精准度

对你意图的理解达到了一个离谱的程度：

- 一张手机随手拍的产品照 → 两句话 → 完整的电商详情页
- 上传电影截图 + 参考图 → 替换人物并保持场景一致
- 上传产品图 → 精修白底电商主图

### 4. 审美进化

最大的审美进化是学会了保留**「不完美」**：

- 胶片颗粒感、闪光灯硬阴影、手持拍摄轻微失焦
- 风格覆盖极广：电影静帧、复古胶片、时尚摄影、像素画、漫画
- **最有效的关键词就是 `photorealistic`** — 模型会主动规避塑料感

### 6. 界面与布局生成

全新的能力维度，能精准复刻各种数字界面：

- 社交媒体截图（抖音、小红书、B 站、TikTok、YouTube）
- App UI 界面（电商首页、音乐播放器）
- 游戏画面（黑悟空等）
- 桌面环境（macOS 浏览器截图、Terminal）

### 7. 🚀 研究驱动的准确性（核心超能力）

这是 GPT Image 2 与其他模型拉开差距的最关键能力：

`gpt-image-2` 接入了 ChatGPT 的深度研究管道 —— 它可以实时联网查找参考资料，并将**真实视觉细节**嵌入输出中。

**实际影响：**

| 能力 | 说明 |
|------|------|
| **Logo 正确渲染** | 不再是扭曲的幻觉，而是准确的品牌标识 |
| **真实产品匹配** | 包装、颜色、比例与真实产品一致 |
| **人物/地点准确** | 编辑引用真实人物、地点、事件时保持正确的时代细节 |
| **App 图标匹配** | Slack、Gmail、Drive、Notion 等图标渲染为真实版本 |
| **技术图表参考** | 芯片布局、架构模式、分子结构参考真实拓扑 |

> **这就是为什么**：编辑排版、多参考组合、密集信息图 —— 都能落地更好，因为模型不是猜"这东西长什么样"。描述真实事物，输出是可用的初稿，而不是"差不多"的近似版。

**示例：30 个真实品牌 Logo 同时渲染**

```text
Tech infographic, landscape. Title "THE AI STACK — 2026" in bold display sans-serif, top center on a warm cream-to-sand gradient background.

Main composition: a precise grid of 30 square cards arranged in 5 rows of 6. Each card contains one real company logo mark in full color rendered with high accuracy at the top, and the company name in clean sans-serif beneath.

The 30 companies in reading order:
Row 1: OpenAI, Anthropic, Google DeepMind, Meta AI, Mistral, xAI
Row 2: Cohere, Perplexity, Hugging Face, DeepSeek, Alibaba Qwen, 01.AI
Row 3: Midjourney, Runway, Pika, Luma, ElevenLabs, Suno
Row 4: Cursor, GitHub Copilot, Replit, Vercel, Lovable, Bolt
Row 5: LangChain, LlamaIndex, Pinecone, Notion AI, Figma AI, Adobe Firefly
```

> 这是研究驱动准确性的极限测试：**30 个不同的真实品牌 Logo 在一张图中** —— 每个都正确渲染颜色、轮廓和文字标记，全部在统一网格上，带有清晰的行标签和干净的排版层次。没有其他图像模型能同时保持这种密度的真实 Logo 精度 + 布局 + 可读性。

---

## 使用入口

### 五种使用方式

| 方式 | 地址 | 说明 |
|------|------|------|
| 官网 | https://chatgpt.com/ | 需要账户 |
| 国内镜像 | https://chatgpt-plus.top/list/#/home | 国内可用 |
| API | https://apipro.maynor1024.live/ | 开发者接入 |
| Codex | https://maynorai.jichiyun.sbs/buy/13 | CLI 工具 |
| 英文版 | https://awesome.gptimage2.asia/en/ | 英文教程 |

---

## 两种模式

### Instant 模式（即时模式）

- 对所有 ChatGPT 用户开放
- 适合日常快速出图

### Thinking 模式（思考模式）

- 需要 ChatGPT Plus / Pro / Business 账户
- 模型会先**联网搜索**、**规划结构**、**自我核查**
- 适合复杂信息图、教育内容、多图连贯场景

---

## 提示词框架

经过大量实测，以下提示词框架效果最佳：

```
[任务类型] + [主体描述] + [风格定义] + [技术参数] + [输出规格]
```

### 五要素详解

| 要素 | 说明 | 示例 |
|------|------|------|
| 任务类型 | 告诉模型做什么 | 海报设计 / 信息图 / 界面截图 / 摄影照片 |
| 主体描述 | 画面核心内容 | 产品、人物、场景、信息结构 |
| 风格定义 | 视觉风格和调性 | 新中式轻奢 / 胶片纪实 / 极简科技 / 手绘水彩 |
| 技术参数 | 光影、材质、构图 | 柔光打光 / 浅景深 / 电影级打光 / octane 渲染 |
| 输出规格 | 比例和分辨率 | 3:4 / 9:16 / 4K / 8K |

### 核心原则

1. **具体 > 模糊**：描述越具体，输出越精准
2. **中文直接说**：不需要翻译成英文，中文提示词效果一样好
3. **给出文字内容**：直接把需要出现在图中的文字写在提示词里
4. **指定风格参考**：用「参考 XX 风格」来锚定审美方向
5. **标注比例和分辨率**：如 `3:4, 4K` 可以控制输出尺寸

---

## 提示词合集

### 一、人像摄影类

#### 1.1 霓虹便利店人像

```
35mm film photography with harsh convenience store fluorescent lighting mixed with colorful neon signs from outside, authentic film grain, high contrast, slight color cast, cinematic street editorial style, intimate medium shot, early 20s sexy Chinese female idol with ultra-realistic delicate refined Chinese features, seductive almond-shaped fox eyes with natural double eyelids, high nose bridge, small sharp V-shaped jawline, flawless porcelain skin with cool ivory undertone and visible specular highlights from fluorescent light, subtle skin texture and micro pores, natural dewy makeup with soft flush on cheeks, glossy natural pink lips slightly parted, subtle natural freckles across nose and cheeks, long dark brown hair in a messy high ponytail with many loose strands falling around face and neck, wearing an oversized white button-up shirt as the only top, unbuttoned at the top with deep cleavage and loosely tied at the waist, paired with a tiny black pleated mini skirt, barefoot in simple white slides, seductive casual leaning pose against the glass door of a 24-hour convenience store at late night, body slightly arched, one leg bent with foot resting against the door frame, the other leg straight, one hand holding a bottle of iced drink, the other hand lightly pulling the hem of her mini skirt, intensely seductive playful yet slightly vulnerable gaze straight at the viewer with soft doe eyes full of quiet temptation and teasing smile, bright cold fluorescent store light from inside mixed with pink and blue neon glow from outside signs, realistic reflections on glass door, blurred convenience store interior with shelves and snacks in background, authentic 35mm film color grading with harsh lighting and neon accents, extremely sharp yet soft skin rendering, natural hair strands, realistic fabric wrinkles and drape on the oversized shirt and mini skirt, no plastic skin, no digital over-sharpening, no airbrushing, no blemishes, no moles, no oily skin, no watermark, no text, authentic late-night convenience store atmosphere
```

#### 1.2 日式温泉旅馆人像

```
35mm film photography, warm vintage Japanese onsen ryokan aesthetic, soft ambient wooden lantern lighting mixed with gentle natural window light, subtle film grain, gentle color shift, high atmosphere editorial style, intimate medium shot, early 20s beautiful Chinese female idol with ultra-realistic delicate refined Chinese features, seductive almond-shaped fox eyes with natural double eyelids, high nose bridge, small sharp V-shaped jawline, flawless porcelain skin with warm ivory undertone, visible subtle skin texture and micro pores, soft natural makeup with dewy glow, subtle rosy flush on cheeks, natural soft pink lips slightly parted, long dark brown hair tied in a loose low bun with some messy strands falling around face and neck, wearing a loose white yukata (traditional Japanese bathrobe) deliberately slipped off one shoulder and loosely tied at the waist, the fabric slightly open revealing smooth skin and subtle cleavage, barefoot, seductive relaxed sitting pose on the edge of a traditional wooden engawa veranda at a vintage onsen ryokan, body slightly turned toward the camera, one leg bent with foot resting on the wooden floor, the other leg gently dangling, one hand lightly holding the yukata collar, the other hand resting on the wooden floor behind her for support, softly arched back to gently accentuate curves, intensely seductive yet gentle and inviting gaze straight at the viewer with soft doe eyes full of quiet temptation and warmth, warm wooden interior with paper sliding doors and distant steaming hot spring in soft focus, gentle rim lighting highlighting skin and fabric texture, authentic vintage film color grading with warm tones, extremely sharp yet soft skin rendering, natural hair strands, realistic fabric wrinkles and drape on the yukata, no plastic skin, no digital over-sharpening, no airbrushing, no blemishes, no moles, no oily skin, no watermark, no text, authentic 35mm film Japanese onsen ryokan atmosphere
```

#### 1.3 韩国偶像 3x3 网格人像

```
9:16 vertical, Korean idol portrait photoshoot, 3x3 grid (nine frames), same person in all images, consistent facial features and styling, soft black mist filter effect, lowered contrast, blooming highlights, subtle glow around light sources
```

**生成效果：**

<img src="https://raw.githubusercontent.com/JerryZ01/gpt-image-2-tutorial/main/assets/9cf568f3-aab1-4c55-bcd5-bee330c0c55e.png" width="400" alt="韩国偶像 3x3 网格人像">

#### 1.4 CCD 相机闪光灯人像

```
mobile phone photo, old CCD camera aesthetic, harsh flash, grainy, dim messy indoor lighting, candid snapshot feeling, slight motion blur, young Korean female idol, soft innocent look
```

**生成效果：**

<img src="https://raw.githubusercontent.com/JerryZ01/gpt-image-2-tutorial/main/assets/d8a47618-645d-46ab-ac8f-38ed08a877f5.png" width="400" alt="CCD 相机闪光灯人像">

#### 1.5 富士胶片草莓色调学校人像

```
Fujifilm strawberry color film simulation, soft pinkish strawberry tone, gentle warm glow, slight film grain, dreamy soft focus background, intimate close-up portrait, young East Asian student, natural minimal makeup, soft realistic skin texture, slight overexposure on highlights, airy and nostalgic atmosphere --ar 3:4
```

### 二、海报插画类

#### 2.1 城市宣传海报

```
一张充满新春喜庆氛围但不失高雅格调的 2026 城市宣传海报。
双重曝光，构图延续了 S 型的流动感；
在条"河流"中，叠加了一个有山有海河的广州城市手绘图，国潮，景色尽在眼底，壮阔雄伟，令人震撼。
广州的地标建筑（广州塔，珠江新城建筑群，珠江，广州城里古建筑，游轮，白云山）。
文字排版优美，大方，字迹清晰完整，尺寸 9:16。
```

**生成效果：**

<img src="https://raw.githubusercontent.com/JerryZ01/gpt-image-2-tutorial/main/assets/eb561e1a-b69b-412c-a4ce-a40f7ab253fc.png" width="400" alt="城市宣传海报">

#### 2.2 复古旅行海报

```
Vintage travel poster of Amalfi Coast, Italy. Retro 1950s graphic design style, hand-drawn illustration, warm Mediterranean colors, terracotta and azure blue, sailboats on the sea, cliffside villages, lemon trees, elegant typography, "VISIT AMALFI" header, classic travel poster composition, 9:16
```

#### 2.3 成都美食地图插画

```
Chengdu food map illustration, colorful infographic style, local specialties labeled in Chinese: hotpot, mapo tofu, dan dan noodles, spicy rabbit head, traditional street food stalls, cartoon-style food icons, map layout with streets and landmarks, warm orange and red tones, playful and appetizing aesthetic, 4K, 3:4
```

#### 2.4 中国风极简 S 型海报

```
Chinese minimalist poster, S-shaped flowing composition, ink wash aesthetic, single color gradient from deep red to soft pink, elegant brushstroke texture, abstract mountain silhouette, one large Chinese character "春" (spring) centered, clean white background with subtle rice paper texture, modern typography integration, Zen-inspired, 9:16
```

#### 2.5 科幻电影海报

```
Epic science fiction movie poster, dark fantasy aesthetic, massive alien mothership descending over futuristic city skyline, neon purple and cyan lighting, dramatic perspective, lens flare, floating debris and smoke, movie title typography "INVASION 2026", cinematic 4K quality, theatrical poster composition, 9:16
```

### 三、电商产品类

#### 3.1 香水电商详情页

```
（有香水垫图）给这个香水产品生成电商中文详情页，9:16，4k
```

#### 3.2 产品精修白底图

```
帮我生成一张图片，将该产品进行精修，可重新打光，精修优化，白色的背景。
```

#### 3.3 高保真电商 App 首页

```
生成一张高保真移动端电商 App 首页界面截图，整体风格参考 2026 年主流中文电商 App，要求界面极其真实，具有完整的手机应用 UI 逻辑与商业设计感。页面顶部为状态栏，包含时间 9:41、5G 信号、电量图标。下面是搜索框区域，左侧为城市选择 杭州，中央是圆角搜索框，提示词为 搜索耳机、咖啡机、运动鞋，右侧有消息图标和扫一扫图标。搜索区下方是横向分类标签，包含 推荐、数码、家电、服饰、美妆、食品、运动、家居，其中 推荐 高亮选中。

首页主体内容必须包含以下结构并排版清晰：
顶部轮播 Banner 一张，主题为 618 预售开启，副标题 每满300减50，画面带商品海报和红色促销氛围
Banner 下方为 10 宫格功能区，图标风格统一，包含 超市、百亿补贴、秒杀、直播、充值中心、到家、领券、品牌馆、全球购、排行榜
中部为 限时秒杀 模块，左侧标题，右侧倒计时 02:14:39，下方三件商品卡片横向排列，每件商品含商品图、标题、现价、原价、已售进度条
下方为 猜你喜欢 双列商品瀑布流，至少 6 张商品卡，每张卡片包含商品图、两行商品标题、价格、月销、店铺名、好评率、券后价标签
底部固定 Tab Bar，包含 首页、分类、购物车、消息、我的，其中 首页 为高亮状态

要求：所有中文文字清晰、可读、接近真实字体，图标统一，间距合理，留白真实，卡片阴影、圆角、分隔线、标签样式高度像真实 App，不要生成手机外壳，只输出纯界面截图，整体必须让人一眼觉得是真实电商 App 截图，而不是概念图
```

#### 3.4 护肤品电商首图

```
高端护肤品电商首图海报，产品名为 澄光维稳精华。整体风格干净、轻奢、科学护肤感强，画面中心是一瓶半透明磨砂玻璃精华液，带淡金色液体和水珠反光，背景为奶白到暖灰渐变，局部有液体流动与微观分子结构装饰。要求同时具备品牌感和卖货感。

海报必须包含以下文案：
澄光 维稳精华
修护屏障 舒缓泛红 细腻透亮
第 2 代升级配方
核心成分 神经酰胺 泛醇 B5 积雪草提取物 微囊脂质体
适合人群 敏感肌 熬夜肌 换季不稳定肌
限时到手价 229 元 买 1 送 3
赠洁面 15ml 赠精华 5ml 赠面霜 10g
左下角小字：实际效果因人而异，请坚持使用

要求重点测试商品卖点、价格、赠品列表、产品名与功能短句的层级。整体要高级，不能土，不要过度直播间风格。
```

### 四、UI 界面类

#### 4.1 一键 UI 生成

```
Design a modern mobile banking app UI interface with clean typography and intuitive navigation. Include: home screen with account balance display, recent transactions list, quick action buttons (transfer, pay, invest), and a bottom navigation bar. Color scheme: deep navy blue with gold accents. Typography: Sans-serif, modern, clear hierarchy. Layout: card-based, rounded corners, subtle shadows. 9:16, 4K
```

#### 4.2 抖音直播截图

```
抖音直播界面截图，主播是一位年轻女性正在介绍口红产品，画面上方显示直播标题"李佳琦口红专场"，左侧有商品卡片和价格信息，右侧有弹幕滚动区域，底部有购买按钮和点赞数，真实直播界面风格，中文文字清晰，9:16
```

#### 4.3 玻璃拟态 UI 设计系统

```
Glassy UI design system showcase, frosted glass effect cards, translucent panels with blur background, soft gradient borders, subtle glow highlights, modern iOS-style aesthetic, floating elements, layered depth, soft shadows, clean white and pastel color palette, responsive grid layout, multiple component examples: buttons, cards, navigation bars, modals, 4K, 9:16
```

#### 4.4 日式 RPG 状态屏

```
Japanese RPG game status screen UI, anime-style character portrait panel on left side, stats display with HP/MP bars and numeric values, equipment slots grid on right, skill icons in bottom row, traditional JRPG aesthetic with modern polish, warm color scheme with gold accents, detailed background art, fantasy game interface, 4K
```

### 五、角色设计类

#### 5.1 动漫风格转换

```
Convert this photo into anime-style character portrait, maintaining original facial features and pose, adding typical anime aesthetics: larger expressive eyes, softer skin, stylized hair with more volume, cleaner outlines, vibrant colors, Japanese animation studio quality, 3:4
```

#### 5.2 Persona5 角色卡

```
Persona 5 style character reference card, bold red and black color scheme, stylized anime portrait with sharp angular features, rebellious aesthetic, character name displayed prominently, personality traits and stats listed below, manga-style shading, dynamic pose, dramatic lighting, 9:16
```

#### 5.3 机甲少女 Key Visual

```
Mecha girl key visual, futuristic cityscape background, anime-style female character with mechanical armor parts, glowing neon circuits, cyberpunk aesthetic, blue and pink color scheme, dynamic action pose, studio-grade illustration quality, high detail on armor panels and joints, 4K, 9:16
```

### 六、信息图类

#### 6.1 科普信息图

```
Create an infographic poster explaining the water cycle for elementary school students. Include 4 stages: evaporation from ocean, cloud formation, rainfall, and river flow back to sea. Use simple cartoon-style illustrations, clear arrows showing process flow, Chinese labels for each stage, bright colors (blue, white, green), friendly and educational tone, 3:4, 4K
```

#### 6.2 人物关系图

```
红楼梦人物关系图，中心是贾宝玉，周围连接林黛玉、薛宝钗、王熙凤、贾母等主要角色，每条连接线标注关系类型（表亲、配偶、仆人等），传统中国画风格边框装饰，水墨淡雅配色，中文标注清晰，结构清晰易懂，4K
```

#### 6.3 食谱流程图

```
辣椒炒肉食谱流程图，6个步骤：1.备料（五花肉切片、辣椒切段）2.热锅冷油 3.炒肉变色 4.加辣椒翻炒 5.调味（生抽、盐）6.出锅装盘。每个步骤配小插画，箭头连接流程，食材清单和用量标注，中文字体清晰，现代扁平化设计风格，暖色调，3:4
```

### 七、社交媒体类

#### 7.1 朋友圈截图

```
生成 OpenAI CEO Sam Altman 在微信朋友圈用中文宣传 ChatGPT Images 2.0 的截图，底下马斯克评论"？？？"，Demis Hassabis 评论"我觉得不如 Nano Banana Pro"，真实朋友圈界面风格，头像和昵称完整，比例 16:9
```

#### 7.2 小红书主页截图

```
小红书个人主页截图，用户名"旅行博主小美"，头像是一位年轻女性，主页包含：粉丝数 128万、获赞数 520万、6宫格笔记预览（美食、旅行、穿搭内容），底部导航栏，真实小红书界面风格，中文清晰，9:16
```

#### 7.3 B 站视频封面

```
B站视频封面设计，主题"GPT-Image-2 全面测评"，左上角UP主头像，右侧大标题文字，底部有播放量数字"10万+"，弹幕数"5000+"，B站标志性的粉色和蓝色配色，游戏/科技频道风格，16:9
```

### 八、品牌设计类

#### 8.1 Logo 设计

```
为"山海咖啡"品牌设计 Logo，融合山海元素：山峦轮廓 + 海浪曲线，简洁现代风格，深绿色为主色调，搭配金色点缀，可用于咖啡杯、包装、门店招牌，输出3种不同构图方案，白底，4K
```

#### 8.2 品牌物料套件

```
山海咖啡品牌视觉套件展示，包含：Logo、咖啡杯设计、外带包装袋、门店海报、员工围裙设计、咖啡豆包装袋，统一品牌色调（深绿+金），现代简约风格，整体展示板布局，4K，9:16
```

### 九、游戏类

#### 9.1 原神战斗 UI

```
原神风格游戏战斗界面截图，左上角角色头像和血条，右侧技能图标（4个元素技能），底部角色切换栏（4个角色头像），中央是Boss战斗场景（巨大怪物），怪物血条显示在顶部，原神标志性的蓝色UI风格，中文文字清晰，16:9
```

#### 9.2 游戏海报

```
武侠游戏宣传海报，水墨画风格背景，中央是一位手持长剑的侠客，标题"剑影江湖"，副标题"2026年度武侠巨作"，传统中国美学与现代游戏设计融合，动态飘逸构图，4K，9:16
```

### 十、杂志编辑类

#### 10.1 杂志封面

```
Editorial magazine cover, portrait orientation. Contemporary 2026 art direction, post-internet aesthetic, bold and saturated.

Full-bleed hero: a photorealistic overhead shot of a matte-black mechanical keyboard partially submerged in a shallow pool of reflective liquid chrome on a polished concrete surface. Dramatic side-lighting from upper-left, saturated electric-violet gradient wash across the background.

Overlay typography, all in bright white:
- Masthead "FORESIGHT" top-left, small all-caps sans-serif
- Date tag top-right, tiny monospace: "VOL. 04 / 2026"
- Hero line "THE END OF THE KEYBOARD" set in huge bold display sans-serif, 60% of frame height

Modern editorial layout, high-contrast, saturated palette. Not a 1990s treatment. No other text.
```

#### 10.2 人物编辑照

```
Cinematic editorial portrait, landscape 16:9. A female barista in her early 30s with short dark hair, wearing a navy denim apron over a simple white t-shirt, concentrated expression, hands working the brass grouphead of a polished La Marzocco Linea Mini espresso machine.

Golden-hour morning light streaming through large industrial windows on the left.

Background: softly blurred but recognizable -- a Blue Bottle Coffee shop interior. The Blue Bottle wordmark visible on a ceramic mug. A Mazzer grinder to the right.

Technical: shot on 50mm lens at f/2.0, shallow depth of field, sharp focus on barista hands. 35mm film grain, warm color grade.

Candid, unposed editorial feel. Documentary photography aesthetic. Render all visible brand marks accurately.
```

### 十一、信息图类

#### 11.1 产品发布信息图

```
Portrait infographic poster on a pale cream-to-lavender gradient background.

Headline "ChatGPT Agents" in bold condensed sans-serif, with "Agents" rendered in vibrant blue-to-purple gradient. Small "NEW" pill badge above.

To the right of title, a 3D-rendered friendly chatbot mascot -- chrome-white sphere with glowing cyan eyes -- surrounded by floating app-icon cards.

Three pill badges below subtitle: "Autonomous", "Reliable", "Works for you".

Section "What they can do" -- a six-card grid. Each card has a small 3D icon, colored title, 3-line description.

Footer: deep blue-to-purple gradient bar with rocket icon and copy "More done. Less effort." OpenAI wordmark on right.

Typography: bold sans-serif headlines, regular sans body. Palette: cream background, navy text, lavender accents. Photorealism in 3D mascot and icons.
```

### 十二、特殊功能类

#### 12.1 360° 全景图

```
360° equirectangular panorama image, view from mountain peak overlooking valley at sunset, dramatic sky with clouds, distant mountains on all sides, realistic lighting with sun position, atmospheric haze, natural landscape photography style, 4K panoramic format
```

#### 12.2 产品爆炸图

```
Sony A7 camera exploded view breakdown, showing all internal components separated but arranged in exploded diagram style, lens elements, sensor, shutter mechanism, circuit boards, battery, buttons and dials, technical illustration style, clean white background, labeled components in Chinese, engineering blueprint aesthetic, 4K
```

---

## 高级技巧

### 技巧 1：photorealistic 是万能钥匙

```
想让输出最自然，最有效的关键词就是 photorealistic。
模型会主动规避塑料感，复刻真实照片的特征。
```

### 技巧 2：善用 Thinking 模式

- 需要联网信息（如品牌知识、人物背景）时，开启 Thinking 模式
- 需要多张连贯图片（如穿搭系列、社交媒体素材）时，开启 Thinking 模式
- 简单出图用 Instant 模式即可，速度快

### 技巧 3：给文字，不要描述文字

```text
# ❌ 错误示范
生成一张有促销信息的奶茶海报

# ✅ 正确示范
生成一张奶茶海报，品牌名为"山川茶事"，新品名为"山柚观音冷泡系列"，价格"中杯 16 元 大杯 19 元"，活动"第二杯半价"
```

### 技巧 4：指定审美方向

```text
# 通过风格参考锚定审美
"参考 1960 年代法国新浪潮电影海报风格"
"采用钢笔淡彩（Pen and wash）技法"
"新中式、轻奢、克制"
"像素画风格 / 复古胶片 / 极简科技"
```

### 技巧 5：垫图 + 编辑，效果翻倍

1. 先上传参考图（垫图）
2. 让 GPT Image 2 生成初稿
3. 点击图片左下角的「编辑」功能进行精细修改
4. 修改可以针对特定区域（如替换品牌、改文字、换人物）

### 技巧 6：利用世界知识

```text
# 模型已经知道这些，不需要你详细描述：
- 各大 App 的界面布局（抖音、小红书、B站、YouTube）
- 品牌的视觉识别系统（星巴克、Apple、特斯拉）
- 真实人物的外观特征
- 游戏的 UI 界面风格

直接说"生成抖音直播截图"或"生成星巴克联名海报"即可。
```

### 技巧 7：蜡笔风格模板

```text
[主体], crayon drawing illustration, hand-drawn with soft waxy texture, visible scribble marks, uneven coloring, playful childlike style, simple shapes, charming imperfections, layered crayon strokes, textured paper surface, warm nostalgic feeling, vibrant colors, clean white background
```

### 技巧 8：商业级 Prompt 模板（推荐）

根据 OpenAI 官方文档，生产级系统应使用标准化格式：

```text
Goal: [目标/用途]
Asset: [资产类型]
Scene: [场景描述]
Subject: [主体描述]
Composition: [构图]
Lighting: [光线]
Materials and styling: [材质与风格]
Constraints: [约束条件]
```

**示例 - 豪华电动车展厅：**

```text
Goal: Create a premium automotive brand image that feels futuristic, elegant, and commercially credible.
Asset: Campaign hero for a luxury electric vehicle launch.
Scene: Nighttime architectural showroom with polished concrete, glass walls, and subtle city reflections.
Subject: One luxury electric vehicle positioned as the hero object, with a clean side-three-quarter profile and visible lighting signature.
Composition: Wide cinematic frame, vehicle clearly dominant, strong horizontal balance, disciplined negative space.
Lighting: Controlled architectural night lighting with crisp body highlights and soft reflected glow from the floor.
Materials and styling: Metallic paint, dark glass, polished concrete, brushed aluminum, premium minimalism.
Constraints: No readable signage, no logo, no people, no traffic, no crowded background, no unrealistic sci-fi effects, no watermark.
```

**示例 - 高端护肤品主视觉：**

```text
Goal: Create a premium skincare hero image that feels expensive, clean, and conversion-ready.
Asset: E-commerce hero banner for a facial serum launch.
Scene: Warm ivory studio set with a round travertine pedestal, shallow water ripples, and soft botanical shadows.
Subject: One frosted glass serum bottle with a brushed champagne cap and a blank label area.
Composition: Centered product, slightly low camera angle, full bottle clearly visible, generous negative space for headline overlay.
Lighting: Soft diffused studio light with luminous highlights and calm luxury mood.
Materials and styling: Frosted glass, brushed metal, polished stone, subtle water shimmer, restrained neutral palette.
Constraints: No logo, no readable text, no hands, no extra props, no duplicate products, no clutter, no deformation, no watermark.
```

---

## API 使用指南

### Python 示例

```python
from openai import OpenAI

client = OpenAI()

# 文生图
response = client.images.generate(
    model="gpt-image-2",
    prompt="a golden retriever wearing sunglasses on a beach",
    n=1,
    size="1024x1024",
    quality="hd",  # 或 "standard"
    response_format="b64_json"  # 或 "url"
)

# 编辑图片
response = client.images.edit(
    model="gpt-image-2",
    image=open("original.png", "rb"),
    mask=open("mask.png", "rb"),
    prompt="replace the background with a mountain scene",
    n=1,
    size="1024x1024"
)

# 变体生成
response = client.images.create_variation(
    model="gpt-image-2",
    image=open("original.png", "rb"),
    n=4,
    size="1024x1024"
)
```

### 参数说明

| 参数 | 说明 |
|------|------|
| `model` | `gpt-image-2`（API 模型名） |
| `prompt` | 文字提示词 |
| `n` | 生成数量（1-4） |
| `size` | `1024x1024`、`1536x1024`、`1024x1536` |
| `quality` | `standard` 或 `hd` |
| `response_format` | `url`（1小时过期）或 `b64_json` |

### 定价

> 官方定价来源：[OpenAI API Pricing](https://openai.com/api/pricing/)

| 类型 | 价格 |
|------|------|
| 图像输入 | $8.00 / 1M tokens |
| 缓存输入 | $2.00 / 1M tokens |
| 输出 | $30.00 / 1M tokens |

**说明：** 推荐 `1024x1024`、`1536x1024`、`1024x1536` 作为默认分辨率。

---

## CLI 工具

### god-tibo-imagen

使用 Codex 认证生成图片的 CLI 工具：

```bash
# 安装
npm install -g god-tibo-imagen

# 使用
gti --prompt "flat blue square icon" --output ./out/blue-square.png

# 带图片输入
gti --prompt "Make this cat wear a hat" --image ./cat.png --output ./cat-hat.png
```

### Python SDK

```python
from gti import Client

client = Client(provider="private-codex")
result = client.generate_image(
    prompt="flat blue square icon",
    model="gpt-image-2",
    output_path="./out.png"
)
```

---

## 🎬 GPT Image 2 × Seedance 2.0 工作流

GPT Image 2 + Seedance 2.0 是目前最强大的 AI 视频工作流之一：
- **GPT Image 2** 负责"画什么"和视觉一致性
- **Seedance 2.0** 负责"怎么动"——将图片动画化为视频

### 标准工作流

1. 用 GPT Image 2 生成分镜/关键帧
2. 导入 Seedance 2.0 使用 Image-to-Video 模式
3. 导出每个片段，在剪辑软件中组合

**GPT Image 2 Prompt：**
```
Create a 6-panel storyboard for a 15-second brand promotional video. Label each panel with a shot description.
Style: cinematic, cool color tone, widescreen 16:9.
Content: the journey of a product from factory to the customer's hands.
```

**Seedance 2.0 Prompt：**
```
Cinematic brand advertisement, slow camera push-in, product centered in frame, warm side lighting, soft background blur, no people, 3 seconds.
```

### 3×3 网格分镜法（重要技巧）

社区发现的关键技巧：将所有分镜面板组合成一张 3×3 网格图再导入 Seedance，失败率远低于逐帧导入。

**GPT Image 2 Prompt：**
```
Generate a single 3×3 storyboard grid image (9 panels total) showing the following continuous action:
[描述你的场景]
Requirements: each panel is clean and self-contained, character positions are consistent across panels, background is consistent, no text labels or annotations.
Output as a single image with all 9 panels arranged in a grid.
```

> **注意：** 输出分镜图用 16:9 避免 Seedance 自动裁剪。帧率设为 24fps 匹合电影标准。

---

## 局限性

GPT Image 2 虽然强大，但仍有以下局限：

| 局限类型 | 说明 |
|---------|------|
| **三维物理逻辑** | 折纸步骤图、魔方复原过程等需要极度严密三维物理逻辑的任务，容易翻车 |
| **密集纹理** | 倾斜表面上的微小细节、极度密集的重复纹理仍会触碰计算边界 |
| **精确箭头图表** | 涉及精确箭头的图表，建议人工核查 |
| **亚洲人一致性** | 对亚洲人面部的一致性保持不如欧美面孔 |
| **透明背景** | 不支持透明背景输出（官方明确说明） |
| **文字渲染** | 文字渲染和精确布局控制虽有改善但仍不完美，文字多的资产需要更严格的提示词 |

---

## API 定价

> 官方定价来源：[OpenAI API Pricing](https://openai.com/api/pricing/)

| 类型 | 价格 |
|------|------|
| 图像输入 | $8.00 / 1M tokens |
| 缓存输入 | $2.00 / 1M tokens |
| 输出 | $30.00 / 1M tokens |

**说明：**
- 不区分分辨率或画质，统一一口价
- 推荐 `1024x1024`、`1536x1024`、`1024x1536` 作为默认分辨率

---

## 商业应用场景

### 行业分类

| 行业 | 应用案例 |
|------|---------|
| **汽车** | 豪华电动车展厅、品牌 Launch 主视觉、官网 Hero |
| **美妆** | 护肤品主视觉、小红书种草图、临床功效图、唇釉色号图 |
| **时尚** | 鞋履 Launch、Lookbook 网格、奢侈品手袋陈列、街头穿搭 |
| **餐饮** | 咖啡拉花生活照、保健品 Packshot、有机茶饮 Pour 场景 |
| **香氛** | 黑曜石香氛 Hero、夜曲系列、高端香水 Landing Page |
| **家居** | 北欧椅生活场景、极简床品 Hero、厨房家电台面 Demo |
| **酒店** | 精品酒店大堂 Editorial、厨师品鉴菜单 Plating |
| **珠宝** | 钻戒微距细节、高级珠宝沙龙、项链 Campaign |
| **科技** | 旗舰手机 Cinematic Launch、高端耳机雕塑感 Hero |
| **季节性** | 618 促销 Banner、圣诞礼品包装、新年红包设计 |

### 商业格式

- **PDP Hero** - 产品详情页主图
- **Marketplace Packshot** - 电商平台产品图
- **Paid Social Static** - 付费社媒静态广告
- **Collection Launch** - 新品系列发布图
- **OOH Billboard** - 户外广告牌
- **Mobile App Homepage** - 移动端 App 首页
- **SaaS Dashboard** - SaaS 产品仪表盘
- **Packaging Unboxing** - 包装开箱展示
- **Lookbook Grid** - 产品目录网格
- **Infographic Editorial** - 编辑型信息图

---

## 参考资源

### GitHub 仓库

- [awesome-gptimage2](https://github.com/xianyu110/awesome-gptimage2) - 中文教程（50+ 案例）
- [awesome-gpt-image-2-prompts](https://github.com/EvoLinkAI/awesome-gpt-image-2-prompts) - 英文案例库（200+ 案例）
- [Awesome-GPT-Image-2-OpenAi](https://github.com/bubblesslayyer-cmd/Awesome-GPT-Image-2-OpenAi) - 商业化提示词库
- [GPT-Image-2-Seedance2-Workflow](https://github.com/EvoLinkAI/GPT-Image-2-Seedance2-Workflow) - 视频工作流
- [gpt-image-2-mcp](https://github.com/Borys520/gpt-image-2-mcp) - MCP 服务器
- [god-tibo-imagen](https://github.com/NomaDamas/god-tibo-imagen) - Node/Python SDK

### 文章来源

1. 蜡笔《熬夜跑了 16 组 GPT Image 2，这些提示词值得你直接拿走》
2. APPSO《刚刚，实测完 GPT-Image-2：设计师没完蛋，但我被 AI 骗麻了》
3. 数字生命卡兹克《实测 GPT-image-2，设计行业真的完蛋了吗？》
4. 甲木未来派《Image2 的六大生产级场景》
5. 量子位《GPT-Image-2 正式发布！设计师可以告别「古法设计」了》
6. 新智元《Images 2.0 登顶王座！大米刻字，生图跨入 GPT-5 时代》

---

## 免责声明

- GPT-Image-2 确实能生成以假乱真的内容，但这也意味着边界更重要
- 证件、试卷等高风险内容，请勿传播
- 很多人并不能分辨 AI 生成的内容，即便带有水印
- 请负责任地使用 AI 图像生成工具

---

<div align="center">

**如果觉得有用，给个 Star 吧！**

Made with ❤️ | Last updated: 2026-04-23

</div>ted: 2026-04-23

</div>