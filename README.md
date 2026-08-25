# Painterly Frame Skill

`Painterly Frame Skill` 是一个把照片或文字场景转译成原创绘画动画画面的 skill。它关注的不是套用滤镜，而是重新设计一张成片：保护人物、姿态、道具状态和场景关系，不等于锁死原画幅、头顶空间、主体占比和色彩面积；在用户未保护这些分布维度时，skill 会主动选择更好的裁切、焦点尺度、负空间与观看路径，再按“大形 → 结构面 → 结构性大笔触 → 材质笔触 → 点睛”的顺序完成画面。

> [!IMPORTANT]
> **仅限个人、非商业使用。** 不允许销售、收费生成、订阅服务、代做、咨询、培训、SaaS/API、公司或客户项目及其他商业化用途。任何商业使用均须事先获得 zcjun（GitHub：[@zcjunn](https://github.com/zcjunn)）的明确书面许可。详见 [个人非商业许可证](LICENSE)。
>
> **Personal, non-commercial use only.** Selling, paid generation, subscriptions, commissions, consulting, training, SaaS/API use, organizational or client work, and all other commercial uses require prior explicit written permission from zcjun. See [LICENSE](LICENSE).

![Painterly Frame 中文流程图](assets/painterly-frame-flow-zh.png)

## 它解决什么问题

- 把人物、风景、建筑、海浪、森林、雪原等输入转成有导演判断的绘画动画画面。
- 保留用户声明的识别锚点，同时允许放大主体、压缩环境、重组负空间、夸张光形或简化重复细节。
- 让色彩由场景负责：根据原图与叙事选择主色场、结构色、焦点色、过渡中性色和可选的色彩碰撞，而不是机械套用固定冷暖或固定暗调。
- 把对比度分配给焦点、支撑结构和背景场：非视觉主体可以发灰、降微对比和边缘密度，但仍保持有色的空间层次。
- 在缩略图尺度就能看出成片与原图的设计差异，同时避免把输入改到无法辨认。

## 正向质量目标

这个 skill 不以“没有动漫化、没有滤镜、没有低多边形”作为完成标准。强风格化结果还必须做出一个缩略图可见的视觉优化：例如改变输出画幅或裁切、让主体或关键道具获得尺度接管、重分配天空/地面/负空间面积、重建大光形与色彩区域，或强化从环境到主体再到动作的观看路径。

来源拓扑与画面分布分开处理：人物身份、动作、视线、道具开合与接触、地标左右关系、遮挡和深度序可以保持不变；输出比例、头顶空间、焦点尺度、面积比例和局部对比度只有在用户明确要求时才锁定。若只说“人物仍在右侧、山仍在左侧”，通常保护的是关系，而不是逐像素坐标。

色彩浓郁来自空间职责，而不是全局提高饱和度：主色场建立气氛，结构色分隔空间，焦点色承担峰值，中性色提供呼吸，深色或亮色锚点稳定画面。降低背景对比度时，优先减少杂乱色相、小硬边、微对比和竞争性纹理，不会自动把成功的大色域洗灰。

大笔触也不是默认错误。只要笔触共同构建云的体积、草木的流向、水流、衣褶、墙面透视或光形，并随材质和远近改变尺度与边缘，它就是结构性大笔触；只有缺少体积和运动依据的装饰性矩形刷板才会被拒绝。

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
- Builds large shapes first, then unequal light/material-derived planes, subordinate transitions, material-owned brush marks and restrained graphic interventions.

### Positive quality target

Avoiding filters, cel shading and mechanical polygons is only the baseline. A strongly stylized result must also make one thumbnail-visible improvement in output ratio or crop, focal scale, area/negative-space allocation, light/colour topology, or viewing path. Recognition topology and image distribution are recorded separately: identity, action, prop state and landmark relationships may remain fixed while unprotected headroom, crop, scale and colour-area shares are deliberately redesigned.

Rich colour comes from spatial ownership—a dominant field, structural counter, focal apex, neutral bridge and a contained dark or light anchor—not from saturating everything. Context is quieted by reducing hue noise, small hard edges, microcontrast and competing texture before bleaching a successful large colour field. Large brushwork is welcome when it interlocks into a named volume or current and changes with material and depth.

### Use it when

- You want a source-aware painterly animated image rather than a photographic filter.
- You want stronger abstraction without losing the main subject, landmark or spatial relationship.
- You need an explicit colour and contrast plan, including high-key, mid-key or low-key results.

Do not use it to copy a named work, character, logo, exact frame or protected production design.

## 使用方法

### 1. 直接描述目标

上传图片，然后用自然语言提出目标即可。skill 会自动选择“新建画面”“编辑目标”“只分析”或“只写提示词”的路径。

推荐至少说明四件事：

1. **必须保留的锚点**：人物身份、人数、动作、道具状态、山峰或建筑的关系；若画幅、坐标、地平线或比例必须精确不变，也要单独说明。
2. **允许改变的范围**：输出画幅、裁切和头顶空间、主体或道具放大、前景遮挡、负空间重组、重复元素合并、光形重构、色彩区域重分配。
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

必须保留：{人物/主体/动作/道具状态/地标关系；哪些位置、比例或画幅必须精确锁定}
允许改变：{输出画幅、裁切、头顶空间、主体放大或缩小、前景遮挡、负空间、重复细节、光形、色彩区域}
第一读取：{观众先看到的主体或关系}
抽象程度：{克制 / 明显 / 强烈}
色彩策略：{保留并整理 / 重新平衡 / 重新脚本；冷暖对比可选}
曝光：{高调 / 中调 / 低调}
避免：{新增人物、文字、标志、复制其他作品的具体设计}
```

## 技能内部的工作顺序

1. **建立 Source Card**：区分观察到的事实与推断，标出身份、姿态、道具状态与接触、朝向、遮挡、地标关系、负空间等识别锚点，以及真正可变的区域。
2. **确定正向质量目标与导演提案**：把拓扑保护和画面分布分开，确定一个主宏观变化和一个辅助变化。变化必须在 128–256 像素缩略图上仍然可见，例如重新选择画幅与裁切、扩大山体或关键道具、让水面变成主导色带、把树冠压成前景拱门，或把一束光重组成视觉走廊。
3. **分配对比度**：焦点拥有最锋利的两到三个对比维度；支撑结构保留中等信息；背景降低局部值差、微对比、硬边和纹理频率，形成统一而有色的背景场。
4. **建立场景色彩表**：主色场、结构色、焦点色、中性色桥接和深色/亮色锚点都要有空间归属。色彩可以是同类色、近单色、互补、分裂互补、局部照明或单纯的明度组织；背景退让不能把成功的大色域洗灰。
5. **建立绘画结构**：先合并成五到九个互相咬合的大形；结构面只能来自朝向、光照、材质边界、褶皱受力或明确的轮廓设计；允许沿体积、流向、透视或动作组织的结构性大笔触；过渡面保持从属；最后才加入较小的材质笔触和点睛。
6. **多尺度质检**：在缩略图、中景和近景分别检查主体读取、构图差异、颜色平衡、背景退让和材质分化，并执行去纹理、分面成因、材质互换、连续描边、巨型刷痕和来源拓扑检查。

完整的面、笔触与材质定义见 [Paint Architecture Contract](references/paint-architecture.md)。

## 不同模型如何保持一致

这里的“一致”指视觉系统和导演判断一致，而不是像素、随机种子或每一笔的位置相同。不同模型必须共享同一份 Portable Render Contract：

完整执行规范见 [Model Consistency Contract](references/model-consistency.md)。

- 相同的主体、数量、动作、空间拓扑和受保护颜色；
- 相同的正向质量目标、所选输出画幅、裁切、焦点尺度和面积关系；这些值可以不同于源图，但跨模型不能各自任意改变；
- 相同的五到九个大色块及其面积、轮廓、遮挡和负空间关系；
- 相同的三组明度，以及主色场、结构色、焦点色和中性桥接色的空间归属；
- 相同的焦点、支撑和背景对比度预算；
- 相同的选择性轮廓语言；不允许默认给完整人物或物体套均匀黑描边；
- 相同的分面拓扑：焦点通常为四到七个大小不等、具有光照/朝向/材质/受力原因的主结构面，而不是赛璐璐两段明暗或随机低多边形；
- 相同的笔触密度梯度：焦点最丰富、支撑约一半、背景约五分之一到三分之一；
- 不同材质各自明确且不可互换的构建方式、笔触尺度、方向、边缘和反光方式；
- 相同的去纹理结果：拿掉所有表面笔触后，轮廓、空间、光向和三组明度仍然成立；
- 相同的结构性大笔触所有权：大型笔触必须共同构建指定体积或流向，而不是被统一缩小或变成装饰性刷板；
- 相同的“非滤镜化”验收：缩略图必须看到大形变化，近景必须看到材质差异，不能只是原照片叠加油画纹理或统一调色。

允许变化的是具体笔触落点、次要纹理、小型自然细节和不改变色彩职责的细微色相偏移。如果某个模型改变第一视觉读取、破坏识别锚点、交换色彩角色、让背景与主体同样抢眼，或让皮肤、布料、金属、草木共享同一种笔触，它就不属于一致结果。出现赛璐璐替代、巨型矩形刷痕、随机三角分面或“只保留相似物件却改变姿态与道具状态”时，只追加对应的一条行为纠偏；一次纠偏后仍失败，就明确判定该模型超出支持范围。随机种子不能跨模型保证一致；需要像素完全相同的区域应使用确定性合成，而不是生成式重绘。

## Cross-model Consistency

Consistency means a shared visual and directorial contract, not identical pixels, seeds or brush placement. Every model is evaluated against the same source topology, five-to-nine macro masses, three value groups, spatial colour roles, contrast tiers and paint-architecture fingerprint: selective contours, unequal causally derived planes, focal-to-context mark-density falloff, non-interchangeable material grammar, and a form read that survives texture removal. Exact brush stamps, secondary texture and small hue shifts may vary only when their visual ownership remains unchanged. A model set is considered consistent only when every output passes the same thumbnail, mid-scale and close-scale checks; a strong average cannot hide one source-literal, cel-shaded, mechanically faceted or globally filtered result.

See [Model Consistency Contract](references/model-consistency.md) for the full portable specification and acceptance boundary.

## 版权边界

这个 skill 只抽象通用的构图、色彩、光线、材质和绘画动画方法，生成原创画面。它不会也不应复制任何受保护作品的角色身份、标志、文字、独特道具、准确场景设计、镜头布局或逐帧画面。若用户提出一比一复刻，应改为描述可观察的视觉关系，并保留原创主体与世界观。

## 本地安装

将本目录放入 skills 目录即可：

```bash
git clone https://github.com/zcjunn/painterly-frame-skill.git ~/.codex/skills/painterly-frame-skill
```

安装后可用自然语言自动触发，或显式写 `$painterly-frame-skill`。

## 项目结构 / Project Structure

```text
painterly-frame-skill/
├── SKILL.md                  # 运行入口：触发范围、路由、主流程与验收契约
├── agents/openai.yaml        # UI 名称、简述和默认调用提示
├── references/               # 按任务条件读取的视觉系统与质量标准
├── assets/                   # README 使用的中英文流程图
├── evals/
│   ├── evals.json            # 效果与回归用例
│   └── trigger-evals.json    # should-trigger / should-not-trigger 用例
├── README.md                 # 面向使用者的双语介绍和安装说明
└── LICENSE                   # 自定义个人非商业许可证
```

该结构采用渐进式加载：执行时先根据 `name` 和 `description` 判断是否触发，再读取 `SKILL.md` 主流程，只有命中具体条件时才加载对应的 `references/`。`assets/` 不作为指令加载；两组 Eval 分别验证“能否正确触发”和“触发后是否真正改善结果”，避免把路由问题与执行质量混在一起。

The repository uses progressive disclosure: discovery metadata selects the skill, `SKILL.md` carries the shared execution path, and individual references are loaded only when their stated conditions apply. Trigger evaluation and effect evaluation are kept separate so routing accuracy is not confused with output quality.

## 许可证 / License

本项目采用自定义的 [Painterly Frame Skill 个人非商业许可证](LICENSE)。它允许自然人为了个人学习、研究、试验或兴趣免费使用和修改，但不允许任何商业、组织或客户用途，也不允许将本 Skill 或其生成服务用于收费。商业使用须事先获得 zcjun 的明确书面许可。

This project uses a custom [Painterly Frame Skill Personal Non-Commercial License](LICENSE). It is not an open-source license: personal non-commercial use is permitted, while commercial, organizational, client, paid-generation, subscription, consulting, training, SaaS/API, and monetized-output uses require prior explicit written permission from zcjun.
