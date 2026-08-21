---
name: ai-manjue-director
description: 总控 AI 漫剧制作流程。用户提到 AI 漫剧、漫剧短片、小说转漫剧、分镜到成片、角色一致性、图生视频或想把故事做成短剧时使用；负责判断当前阶段、调用或衔接 ai-manjue-story、ai-manjue-assets、ai-manjue-storyboard、ai-manjue-video-shot、ai-manjue-edit-qc，并阻止跳过关键验收。
---

# AI 漫剧总控

把故事稳定地推进到可发布成片。核心原则：先锁故事，再锁资产，再做分镜，再生成视频，最后剪辑验收。

## 先做版权闸门

开始前确认素材属于用户本人、已获授权，或仅用于非公开学习。未授权网络小说、真人照片、明星肖像和商业素材不能直接进入商用生产。若权限不清，先停在方案层并标注风险。

## 阶段路由

1. 没有可拍故事：调用 `ai-manjue-story`。
2. 已有剧本但没有角色/场景/道具：调用 `ai-manjue-assets`。
3. 已有资产但没有逐镜头执行表：调用 `ai-manjue-storyboard`。
4. 已有分镜图，要生成动态片段：调用 `ai-manjue-video-shot`。
5. 已有视频、配音和音乐：调用 `ai-manjue-edit-qc`。
6. 用户只要求其中一段时，只调用对应 Skill，不强行跑完整链路。

## 推荐首轮规模

新项目先做 60～90 秒、8～15 镜头的试片。不要一开始就做 5～10 分钟；先验证角色稳定性、镜头连续性、视频成功率和声音节奏。

## 统一项目结构

```text
manju-project/
├── 00-intake.md
├── 01-story.md
├── 02-script.md
├── 03-assets/
│   ├── characters.md
│   ├── scenes.md
│   ├── props.md
│   └── asset-registry.md
├── 04-storyboard.md
├── 05-keyframes/
├── 06-video-prompts/
├── 07-clips/
├── 08-edit-sheet.md
└── 09-qc-report.md
```

## 每阶段交接

阶段结束时只输出四项：`状态`、`已完成文件`、`待解决问题`、`下一阶段输入`。没有通过闸门时，不宣称完成。

## 完成判定

最终成片必须通过：故事可理解、镜头顺序正确、角色/场景/道具无明显跳变、配音与字幕对应、音效有动作依据、手机观看可读、版权边界清楚。

