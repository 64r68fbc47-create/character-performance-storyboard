# Changelog

本文件记录仓库对外可见的变更。版本号遵循语义化（MAJOR.MINOR.PATCH）。

## [Unreleased]

### Changed

- `skills/performance-coach/SKILL.md` 改为本机完整版（65739 字节）。含模块5（表演内容生成）、**模块6：角色文档读写与关系演进**、模块7（技术参数嵌入）。旧文件 38900 字节，只有模块1–4，来自 bot 现装精简版，不再作为准。
- `skills/character-creator/SKILL.md` 改为本机 `character_create_skill.md`（9028 字节），静态区 / 动态区与模块6文档格式对齐（`SCENE-XXX` 记忆条目、关系档位、回写边界）。
- `references/` 整目录与完整包一致。`platform-adapter.md`、`demo-storyboard.md` 完整包已含，予以保留。未发现 AppleDouble `._*`。

### Notes

- **禁止再用精简版覆盖。** 以后维护这两套 skill，以本机「人物创建+叙事表演剧本分镜 Skill（完整版）」为准，不要用 bot 现装的约 39KB performance-coach 当源再拷回来。
- 待定：Topics 是否补 `kling` / `jimeng` / `hailuo` / `storyboard` 等。不再把「再精简 references」当作默认方向。

## [0.1.0] — 2026-10-15

### Added

- 公开仓：https://github.com/64r68fbc47-create/character-performance-storyboard （public，`main`）
- GitHub Release / tag `v0.1.0`：https://github.com/64r68fbc47-create/character-performance-storyboard/releases/tag/v0.1.0
- 发布骨架：README、LICENSE（MIT）、INSTALL、RELEASE-CHECKLIST、FILE-MANIFEST、examples 索引
- 草稿复制 `skills/character-creator/`（SKILL.md + references ×4）
- 草稿复制 `skills/performance-coach/`（SKILL.md + references ×11）
- 标明 skills 为预览副本，源 workflows 正文未改
- 硬卖点 README + `docs/卖点详解.md`（能力边界裁切）已同步（commit `2bcf95d`）

### Notes

- 联系邮箱（文档用）：主联系 yuan-ip@mail.grokbot.com；抄送/备用 leonardy_2026@qq.com  
- 版权：Copyright (c) 2026 原
- 仓库 Description / Topics（ai-video, character, memory, performance, seedance）已在 GitHub 设置
