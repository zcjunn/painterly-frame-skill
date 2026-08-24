# Painterly Frame Skill

`Painterly Frame Skill` 是一个把照片或文字场景转译成原创绘画动画画面的 skill。它关注的不是套用滤镜，而是重新设计一张成片：先判断视觉主体、构图压力和颜色关系，再用大色面、分面笔触、材质化边缘和少量图形标记完成画面。

![Painterly Frame 中文流程图](assets/painterly-frame-flow-zh.png)

## 它解决什么问题

- 把人物、风景、建筑、海浪、森林、雪原等输入转成有导演判断的绘画动画画面。
- 保留用户声明的识别锚点，同时允许放大主体、压缩环境、重组负空间、夸张光形或简化重复细节。
- 让色彩由场景负责：根据原图与叙事选择主色场、结构色、焦点色、过渡中性色和可选的色彩碰撞，而不是机械套用固定冷暖或固定暗调。
- 把对比度分配给焦点、支撑结构和背景场：非视觉主体可以发灰、降微对比和边缘密度，但仍保持有色的空间层次。
- 在缩略图尺度就能看出成片与原图的设计差异，同时避免把输入改到无法辨认。

## 适合使用的场景

- “把这张照片变成有导演式主体重构的绘画动画关键帧。”
- “保留人物和山的位置，但放大山体、降低背景细节，让主体更有压迫感。”
- “把海浪抽象成几块有方向的青绿色形体，保留原来的俯拍关系。”
- “把雪景做成高调、粉蓝和暖光的画面，不要强行压成夜景。”
- “分析这张图的视觉主体和颜色关系，只输出可执行的生成提示词。”

不适合用于：忠实修图、逐像素复原、严格的纪录片拓扑保持，或复制任何已知作品的角色、标志、台词、道具、场景设计和准确镜头。

## English Introduction

`Painterly Frame Skill` is a style-led image transformation skill. It turns a supplied photograph or text scene into an original painterly animated frame by redesigning attention, colour balance, macro shape and material marks instead of applying a generic filter.

![Painterly Frame English workflow](assets/painterly-frame-flow-en.png)

### What it does

- Preserves declared recognition anchors while allowing controlled changes to scale, negative space, light shape and repeated detail.
- Assigns colour by scene function: dominant field, structural counter, focal accent, neutral bridge and optional colour collision.
- Gives the focal event the strongest useful contrast while lowering background microcontrast, edge density and texture frequency.
- Builds large shapes first, then adds faceted planes, material-specific brush marks and restrained graphic interventions.

### Use it when

- You want a source-aware painterly animated image rather than a photographic filter.
- You want stronger abstraction without losing the main subject, landmark or spatial relationship.
- You need an explicit colour and contrast plan, including high-key, mid-key or low-key results.

Do not use it to copy a named work, character, logo, exact frame or protected production design.

## 使用方法

### 1. 直接描述目标

上传图片，然后用自然语言提出目标即可。skill 会自动选择“新建画面”“编辑目标”“只分析”或“只写提示词”的路径。

推荐至少说明四件事：

1. **必须保留的锚点**：人物身份、人数、动作、山峰位置、地平线、建筑关系、文字等。
2. **允许改变的范围**：主体放大、前景遮挡、负空间重组、重复元素合并、光形重构、色彩重脚本。
3. **第一视觉读取**：观众最先看到什么，或希望画面产生什么压力与方向。
4. **色彩倾向**：保留原色、重新平衡、或完全重写；是否允许色彩碰撞。冷暖对比不是必选项。

### 2. 显式调用

也可以直接写：

```text
$painterly-frame-skill
```

然后补充输入图、保留锚点、抽象程度和输出要求。

### 3. 可复制的请求模板

```text
使用 $painterly-frame-skill。
把这张图转成一张原创绘画动画关键帧，输出一张无边框成片。

必须保留：{人物/主体/地标/位置/动作/比例}
允许改变：{主体放大或缩小、前景遮挡、负空间、重复细节、光形、色彩区域}
第一读取：{观众先看到的主体或关系}
抽象程度：{克制 / 明显 / 强烈}
色彩策略：{保留并整理 / 重新平衡 / 重新脚本；冷暖对比可选}
曝光：{高调 / 中调 / 低调}
避免：{新增人物、文字、标志、复制其他作品的具体设计}
```

## 技能内部的工作顺序

1. **建立 Source Card**：区分观察到的事实与推断，标出识别锚点、可变区域、主体和层次。
2. **写导演提案**：确定一个主宏观变化和一个辅助变化。变化必须在 128–256 像素缩略图上仍然可见，例如扩大山体、让水面变成主导色带、把树冠压成前景拱门，或把一束光重组成视觉走廊。
3. **分配对比度**：焦点拥有最锋利的两到三个对比维度；支撑结构保留中等信息；背景降低局部值差、微对比、硬边和纹理频率，形成统一而有色的背景场。
4. **建立场景色彩表**：主色场、结构色、焦点色、中性色桥接和可选回声色都要有空间归属。色彩可以是同类色、近单色、互补、分裂互补、局部照明或单纯的明度组织。
5. **先做大形，再做材质**：先合并成五到九个互相咬合的大色块，再加入岩石、木材、皮肤、水、雪、雾等各自的笔触和边缘逻辑。
6. **多尺度质检**：在缩略图、中景和近景分别检查主体读取、构图差异、颜色平衡、背景退让、材质分化和无意新增元素。

## 版权边界

这个 skill 只抽象通用的构图、色彩、光线、材质和绘画动画方法，生成原创画面。它不会也不应复制任何受保护作品的角色身份、标志、文字、独特道具、准确场景设计、镜头布局或逐帧画面。若用户提出一比一复刻，应改为描述可观察的视觉关系，并保留原创主体与世界观。

## 本地安装

将本目录放入 skills 目录即可：

```bash
git clone https://github.com/zcjunn/painterly-frame-skill.git ~/.codex/skills/painterly-frame-skill
```

安装后可用自然语言自动触发，或显式写 `$painterly-frame-skill`。
