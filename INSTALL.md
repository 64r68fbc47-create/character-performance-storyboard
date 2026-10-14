# 安装说明

把本仓库 `skills/` 下两套 skill **整目录复制**到 Cursor / Grok Bot 的 workflows（或等价 skill）目录。

> `skills/` 是发布骨架里的**草稿副本**。正式环境若已有同名目录，先备份再覆盖。

## 要复制的路径

| 仓库内路径 | 安装到（示例） |
|------------|----------------|
| `skills/character-creator/`（含 `SKILL.md` + `references/`） | `<agent-data>/workflows/character-creator/` |
| `skills/performance-coach/`（含 `SKILL.md` + `references/`） | `<agent-data>/workflows/performance-coach/` |

`<agent-data>` 常见位置：

- Grok Bot / Cursor：以你本机 `agent-data/workflows` 根目录为准（下文用 `<agent-data>`）
- 其他环境：以你本机 Cursor / Agent 文档中的 workflows 根目录为准

## 推荐命令

在仓库根目录执行（把目标路径换成你的）：

```bash
# 人物创建
cp -a skills/character-creator <agent-data>/workflows/character-creator

# 叙事表演剧本分镜
cp -a skills/performance-coach <agent-data>/workflows/performance-coach
```

若目标已存在且只需更新：

```bash
rsync -a --delete skills/character-creator/ <agent-data>/workflows/character-creator/
rsync -a --delete skills/performance-coach/ <agent-data>/workflows/performance-coach/
```

## 安装后检查

1. 每个目录下有 `SKILL.md`。  
2. `references/` 齐全（人物创建约 4 个 md；分镜约 11 个 md）。  
3. 在对话里用触发语试一次（见根 README）。  
4. 建议先跑人物创建出档，再跑分镜，验证联动。

## 不改什么

- 不要手改 `SKILL.md` 正文 unless 你明确要二次开发。  
- 本仓库草稿与正式 workflows 源目录请分开管理，避免把本地私密路径写回开源副本。
