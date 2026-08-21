# cinematic-story-director

把一句故事、普通画面或参考图转化为有叙事动机、可生成、可验收的电影镜头方案。

## 什么时候调用

- 故事转电影镜头、连续分镜、参考图电影语言重构
- 图生视频首帧、CATRL、运镜、微表情和演技调度
- 《甲申：余烬之末》《流芳》等明末历史叙事画面

## 调用方式

自然语言：

```text
用 cinematic-story-director，把这段故事设计成可直接生成的叙事镜头，并说明镜头为何成立。
```

显式调用：

```text
使用 $cinematic-story-director 分析这张参考图的 Shot / Light / Space / Story，并给出首帧和 6 秒视频方案。
```

## 核心方法

- **Shot**：观众站在哪里，和人物及事件保持什么距离。
- **Light**：光从哪里来，哪些信息被显露或隐藏。
- **Space**：前景、中景、后景和留白承担什么信息。
- **Story**：画面之前发生了什么，之后可能发生什么。
- 视频任务再用 CATRL 拆分 Character、Action、Texture、Render、Lighting，并把运镜轴与演技轴分开。

## 默认输出

镜头目的、四维判断、决定性瞬间、完整提示词、首帧理由、动态时序、验收重点和失败后的降级顺序。

## 与其他 Skill 的关系

- `cinematic-story-director`：上游决定镜头为什么存在。
- `cinematic-image2-spec`：下游把决定性瞬间落实为 Image 2 静帧摄影规格。

## 边界

不声称复刻具体电影、导演或摄影师的独特风格；历史细节按史料明确、交叉支持、合理推演、视觉提案和待确认分级，不把未核实内容包装成史实。

## 本机位置

`~/.codex/skills/cinematic-story-director`
