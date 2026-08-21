# AI Manju Production Skills

一套面向 AI 漫剧、AI 短视频和图生视频生产的 Skill 合集。

它把一条完整生产链拆成可复用的中间产物：

```text
故事 / 剧本
  → 角色、场景、道具资产
  → 导演判断与摄影规格
  → 分镜首帧
  → 故事板投产卡
  → 图生视频
  → 高清修复
  → 剪辑与声音
  → 质检与归档
```

## 包含的 Skills

| Skill | 用途 |
|---|---|
| `ai-manjue-director` | AI 漫剧总控与阶段路由 |
| `ai-manjue-production-pipeline` | 从剧本推进到可执行生产包 |
| `ai-manjue-story` | 故事、人物压力和单集剧本 |
| `ai-manjue-assets` | 角色、场景、道具和一致性锚点 |
| `ai-manjue-storyboard` | 逐镜头分镜和故事板投产卡 |
| `ai-manjue-video-shot` | 首帧到图生视频的动作提示词 |
| `ai-manjue-edit-qc` | 剪辑、声音、字幕和成片质检 |
| `cinematic-story-director` | Shot / Light / Space / Story 叙事镜头设计 |
| `cinematic-image2-spec` | GPT Image 2 电影静帧摄影规格 |

## 推荐使用顺序

总控入口优先使用 `ai-manjue-director` 或 `ai-manjue-production-pipeline`。

```text
ai-manjue-story
→ ai-manjue-assets
→ cinematic-story-director
→ cinematic-image2-spec
→ ai-manjue-storyboard
→ ai-manjue-video-shot
→ ai-manjue-edit-qc
```

## 安装

### Codex / 本地 Agent

将 `skills/` 下需要的 Skill 文件夹复制到本机的 Skill 目录，例如：

```text
%USERPROFILE%\.codex\skills\
%USERPROFILE%\.agents\skills\
```

### Git clone

```powershell
git clone https://github.com/xiajixi76-beep/ai-manjue-production-skills.git
```

## 生产边界

- 先锁故事，再锁角色和场景资产，再做首帧和视频。
- 每个视频子镜头优先控制在 2～5 秒，并只安排一个主要物理动作。
- 角色、场景、服装、道具和光线必须经过人工确认后才进入批量生成。
- 只使用本人、已获授权或明确用于非公开学习的素材。
- GPT 负责导演、拆解、提示词、交接和验收；图像/视频模型负责实际生成。

## 相关独立仓库

- [cinematic-story-director-skill](https://github.com/xiajixi76-beep/cinematic-story-director-skill)
- [cinematic-image2-spec-skill](https://github.com/xiajixi76-beep/cinematic-image2-spec-skill)

本合集是统一安装与备份入口；独立仓库仍可单独使用。

