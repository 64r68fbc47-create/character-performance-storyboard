# character-performance-storyboard

把「人物创建」与「叙事表演剧本分镜」两套 Cursor / Grok Bot skill 打包开源，方便安装、联动与二次分发。

> **状态：发布骨架草稿（待命）**  
> `skills/` 下为源目录整份复制的**草稿预览副本**，非正式 Release。  
> 源正文仍在本机 `agent-data/workflows/`；未获确认前勿擅自改 skill 正文。

## 两个 skill 各干什么

| Skill | 目录 | 一句话 |
|--------|------|--------|
| **人物创建** | `skills/character-creator/` | 生成标准化、可复用的角色档案（身份、人格、面具、记忆、情绪），供分镜与对话调用。 |
| **叙事表演剧本分镜** | `skills/performance-coach/` | 为可灵 / 即梦 / 海螺等写表演向分镜与可复制 Prompt（台词断句、微表情、肢体、光影空间）。 |

## 联动：人物档案 → 分镜

1. 先用 **人物创建** 出角色档案（快速出档或深挖）。  
2. 再启动 **叙事表演剧本分镜**；有档案则跳过角色问答，直接问戏目标 / 场景 / 风格 / 模型。  
3. 分镜里重大情绪或认知变化，可回写档案记忆层，保持全剧一致。

## 怎么安装

详见 [INSTALL.md](./INSTALL.md)。摘要：

```bash
# 复制到本机 workflows（路径按你的环境调整）
cp -a skills/character-creator   <你的 agent-data/workflows>/character-creator
cp -a skills/performance-coach   <你的 agent-data/workflows>/performance-coach
```

Cursor / Grok Bot 识别 `workflows/<name>/SKILL.md` 后即可用触发语调用。

## 触发语示例

**人物创建**

- 帮我创建一个角色  
- 生成人物设定 / 做角色档案  
- 给剧本写人物小传  

**叙事表演剧本分镜**

- 帮我写一段 AI 视频分镜  
- 生成可灵用的表演 prompt  
- 做一组双人戏分镜 / 给即梦出个动漫独白镜头  
- 启动叙事表演剧本分镜 skill / 我要做剧本分镜  

## 示例与参考

见 [examples/README.md](./examples/README.md)，指向各 skill 内 `references/` 的 demo。

## 文件清单与发布

- [FILE-MANIFEST.md](./FILE-MANIFEST.md) — 源路径 → 仓库路径  
- [RELEASE-CHECKLIST.md](./RELEASE-CHECKLIST.md) — 发布前核对  
- [CHANGELOG.md](./CHANGELOG.md) — 版本草稿  

## 许可证

[MIT](./LICENSE) — Copyright (c) 2026 感原林  
联系：526006733@qq.com  

欢迎 Star / Issue / PR；产品方向与是否拆仓以仓库维护者确认为准。
