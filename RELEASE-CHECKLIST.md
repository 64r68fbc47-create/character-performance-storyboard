# 发布前清单

用于 GitHub 仓库 `character-performance-storyboard` 首发 / 后续 Release。勾一项做一项。

## 文档与许可

- [ ] README 一句话、两 skill 说明、安装、联动、触发语已更新  
- [x] LICENSE 为 MIT；版权行 `Copyright (c) 2026 原`  
- [ ] INSTALL.md 路径与复制命令可粘贴即用  
- [ ] examples/README.md 指向真实 references demo  
- [ ] FILE-MANIFEST.md 与仓库树一致  
- [ ] CHANGELOG.md 已填本版条目（从 Unreleased 挪出）

## 内容与敏感信息

- [ ] `skills/` 为确认过的副本（非整仓误拷私货）  
- [ ] 扫描：无本机绝对路径（如 `/home/box/...`）、无私人邮箱/token/密钥、无未授权第三方全文  
- [ ] SKILL 正文未夹带仅内部用的账号/群聊/总监指令  
- [ ] demo 角色与分镜示例可公开（无真实隐私）

## 版本与 GitHub

- [ ] 确认：合仓发布 **或** 先开哪一套（用户拍板）  
- [x] GitHub 仓库已建：`character-performance-storyboard`  
- [ ] 默认分支、Description、Topics（如 `cursor-skill` `ai-video` `storyboard`）  
- [ ] 打 tag，例如 `v0.1.0`  
- [ ] 首条 Release notes 已写（可用下方模板）

## 首条 Release notes 模板（可直接粘贴）

```markdown
## character-performance-storyboard v0.1.0

首次公开打包两套 Cursor / Grok Bot skill：

- **人物创建**（character-creator）：标准化角色档案  
- **叙事表演剧本分镜**（performance-coach）：表演向分镜 + 可灵/即梦/海螺 Prompt  

### 安装
见仓库 INSTALL.md：将 `skills/*` 复制到本机 `agent-data/workflows/`。

### 许可
MIT © 2026 原

### 说明
本版为可安装预览包。产品方向与拆仓与否以维护者后续说明为准。
```

## 发布后

- [ ] README 徽章 / 链接可用  
- [ ] 用干净环境按 INSTALL 装一遍冒烟  
- [ ] 收集 Issue：安装路径、触发语、模型适配

## GitHub Topics 备选（定稿推仓时勾）

英文 Topics（仓库 Settings → Topics，约 8～12 个）：

- `ai-video`
- `kling`
- `jimeng`
- `hailuo`
- `storyboard`
- `character`
- `prompt`
- `performance`
- `cursor-skills`（若平台认）
- `agent-skills`

README / 仓库描述里留给中文检索的词（不必全当 Topic）：

- 人物档案、表演分镜、可灵、即梦、海螺、AI 视频分镜

描述草案（About 一行）：`人物档案 + 表演向分镜 Skill：可灵 / 即梦 / 海螺可复制 Prompt`

