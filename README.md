# GPT-Image-2 完全教程

> 从零到一掌握 OpenAI 最新图像生成模型的全攻略
>
> 整合官方文档、社区最佳实践、200+ 精选提示词、覆盖 10 大应用场景

[![GitHub](https://img.shields.io/badge/GitHub-Repository-black?style=for-the-badge)](https://github.com/JerryZ01/gpt-image-2-tutorial)
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

2026 年 4 月 22 日，OpenAI 正式发布 **ChatGPT Images 2.0**（API 模型名 `gpt-image-1`），奥特曼称之为「从 GPT-3 到 GPT-5 的飞跃」。

它是 OpenAI 首个具备**思考能力**的图像模型，在 Arena 盲测榜单中以断层优势登顶全球第一，领先第二名超过 240 分。

### 关键参数

| 特性 | 详情 |
|------|------|
| 知识截止 | 2025 年 12 月 |
| 最大分辨率 | 2K（API Beta） |
| 宽高比 | 3:1 ~ 1:3 |
| 单次生成 | 最多 8 张连贯图（Thinking 模式） |
| 生成速度 | 约 3 秒/张（Instant 模式） |
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

### 5. 界面与布局生成

全新的能力维度，能精准复刻各种数字界面：

- 社交媒体截图（抖音、小红书、B 站、TikTok、YouTube）
- App UI 界面（电商首页、音乐播放器）
- 游戏画面（黑悟空等）
- 桌面环境（macOS 浏览器截图、Terminal）

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
- 生成速度约 3 秒/张
- 适合日常快速出图

### Thinking 模式（思考模式）

- 需要 ChatGPT Plus / Pro / Business 账户
- 模型会先**联网搜索**、**规划结构**、**自我核查**
- 单次最多生成 **8 张角色和对象连贯**的系列图片
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

#### 1.4 CCD 相机闪光灯人像

```
mobile phone photo, old CCD camera aesthetic, harsh flash, grainy, dim messy indoor lighting, candid snapshot feeling, slight motion blur, young Korean female idol, soft innocent look
```

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

### 十、特殊功能类

#### 10.1 360° 全景图

```
360° equirectangular panorama image, view from mountain peak overlooking valley at sunset, dramatic sky with clouds, distant mountains on all sides, realistic lighting with sun position, atmospheric haze, natural landscape photography style, 4K panoramic format
```

#### 10.2 产品爆炸图

```
Sony A7 camera exploded view breakdown, showing all internal components separated but arranged in exploded diagram style, lens elements, sensor, shutter mechanism, circuit boards, battery, buttons and dials, technical illustration style, clean white background, labeled components in Chinese, engineering blueprint aesthetic, 4K
```

---

## 高级技巧

### 1. 参考图编辑

上传一张图片，然后用文字描述修改：

```
（上传产品图）帮我生成一张图片，将该产品进行精修，可重新打光，精修优化，白色的背景。
```

### 2. 多图融合

上传多张人物照片，生成合影：

```
（上传三张单人照和一张参考合照）让前三个人物模仿参考图里的姿势，一起拍 vlog 合照。
```

### 3. 角色一致性

上传一张人物照，生成多套穿搭：

```
（上传人物照片）为这个人物生成5套不同风格的穿搭照片，保持脸部特征一致，分别展示：休闲风、职场风、运动风、街头风、度假风。
```

### 4. 手写文字

```
用普通人的笔迹抄写《定风波·莫听穿林打叶声》，手写感自然，不要贴图感。
```

### 5. 信息图生成

```
生成一张介绍 GPT Image 2 核心能力的中文百科/信息图海报，模块化布局，图鉴感强。
```

---

## API 使用指南

### Python 示例

```python
from openai import OpenAI

client = OpenAI()

# 文生图
response = client.images.generate(
    model="gpt-image-1",
    prompt="a golden retriever wearing sunglasses on a beach",
    n=1,
    size="1024x1024",
    quality="hd",  # 或 "standard"
    response_format="b64_json"  # 或 "url"
)

# 编辑图片
response = client.images.edit(
    model="gpt-image-1",
    image=open("original.png", "rb"),
    mask=open("mask.png", "rb"),
    prompt="replace the background with a mountain scene",
    n=1,
    size="1024x1024"
)

# 变体生成
response = client.images.create_variation(
    model="gpt-image-1",
    image=open("original.png", "rb"),
    n=4,
    size="1024x1024"
)
```

### 参数说明

| 参数 | 说明 |
|------|------|
| `model` | `gpt-image-1`（API 模型名） |
| `prompt` | 文字提示词 |
| `n` | 生成数量（1-4） |
| `size` | `1024x1024`、`1536x1024`、`1024x1536` |
| `quality` | `standard` 或 `hd` |
| `response_format` | `url`（1小时过期）或 `b64_json` |

### 定价

| 类型 | 价格 |
|------|------|
| Standard 1024×1024 | ~$0.01/张 |
| HD 1024×1024 | ~$0.04/张 |

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
    model="gpt-5.4",
    output_path="./out.png"
)
```

---

## 局限性

### 1. 文字稳定性

- 长文本仍可能有错字
- 小字号文字可能模糊
- 复杂排版可能错位

### 2. 人物渲染

- 手部偶尔变形
- 真实人物不能生成可识别照片
- 动态姿势可能有瑕疵

### 3. 安全限制

- 不能生成暴力、成人内容
- 不能生成品牌 logo、知名 IP 角色
- 不能生成证件、试卷等敏感内容

### 4. API 限制

- url 链接 1 小时过期
- 有 rate limit
- Beta 版本可能变化

---

## 最佳实践

### 1. 提示词优化

- ✅ 具体描述光线、材质、构图
- ✅ 直接写中文文字内容
- ✅ 指定比例和分辨率
- ❌ 避免模糊描述如"好看"、"漂亮"
- ❌ 避免过长的提示词（建议 < 500 字）

### 2. 生成策略

- 先用 `standard` 预览，满意后再用 `hd`
- 多生成几张选最好的
- 用 `seed` 参数复现结果

### 3. 编辑技巧

- 上传清晰的原图
- 用简洁的语言描述修改
- 分步骤处理复杂修改

### 4. 成本控制

- 批量生成时注意 rate limit
- 及时下载 url 图片避免过期
- 合理使用 quality 参数

---

## 参考资源

### GitHub 仓库

- [awesome-gptimage2](https://github.com/xianyu110/awesome-gptimage2) - 中文教程
- [awesome-gpt-image-2-prompts](https://github.com/EvoLinkAI/awesome-gpt-image-2-prompts) - 英文案例库
- [gpt-image-2-skill](https://github.com/Wangnov/gpt-image-2-skill) - CLI 工具
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

</div>