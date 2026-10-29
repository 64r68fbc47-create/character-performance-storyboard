# character-performance-storyboard

> **一句话定位**  
> 从一句人设粗描述，到可直接粘贴进可灵 / 即梦 / 海螺的表演级分镜 Prompt——角色带记忆、关系有分寸、情绪会连锁、光影不漂移。

把「人物创建」与「叙事表演剧本分镜」两套 Cursor / Grok Bot skill 打包开源。

> **状态：仓库内 skills 以本机完整版为准（含模块6）**  
> GitHub Release：https://github.com/64r68fbc47-create/character-performance-storyboard/releases/tag/v0.1.0  
> 来源：本机 `Desktop/原素材/skill/人物创建+叙事表演剧本分镜Skill（完整版）`。`skills/performance-coach/SKILL.md` 为完整版（约 65KB），含模块5、**模块6：角色文档读写与关系演进**、模块7。`skills/character-creator/SKILL.md` 来自本机 `character_create_skill.md`，文档格式与模块6对齐。  
> **禁止再用 bot 现装精简版覆盖**（约 39KB / 38900 字节，只有模块1–4）。精简版不是准。

## 这是什么 / 不是什么

| 是 | 不是 |
|----|------|
| Skill **文档套件**（Markdown 流程 + 输出模板） | 成片 App / 无限画布 / 视频算力 |
| 装进助手 workflows，用触发语驱动吐文本 | 替你调可灵 / 即梦 / 海螺 API |

## 硬卖点（5）

1. **双 Skill 闭环**：人物创建出与模块6对齐的标准人物文档 → 叙事表演分镜导入文档出分镜 → 事件定稿后由模块6**回写**动态区；静态人设不漂。  
2. **记忆含关系**：文档分静态区（只读）与动态区（记忆档案 + 人际关系快照）。记忆为 `SCENE-XXX` 整段条目；关系按三维度打分，客观档位取双方主观最小值。  
3. **输出即 Prompt**：每镜正向 + 反向可复制；表演优先（台词断句 / 微表情 / 肢体）＞ 光影 ＞ 时长；适配可灵 / 即梦 / 海螺。最终输出禁止写入 MBTI、抑制等级等内部术语。  
4. **空间与光影不漂**：跨镜接续人物物理状态；灯光基调整场固定，靠走位变更受光，不为情绪改灯。  
5. **分步收集，有文档则导入**：一次一问（人数、人设、剧情目的、场景、情绪→表演→视听三阶确认）。已有标准人物文档则导入解析，缺字段再补问。

更细的能力边界与推介示例见 [docs/卖点详解.md](./docs/卖点详解.md)。

### 技能表

| Skill | 目录 | What it does |
|--------|------|----------------|
| **人物创建** | `skills/character-creator/` | 与模块6对齐的标准人物文档：静态区（基础人设 / 决策规则 / 情绪行为表 / 专属标识库 / 关系档位行为偏移）+ 动态区框架（记忆档案 / 人际关系快照）。 |
| **叙事表演剧本分镜** | `skills/performance-coach/` | 完整版模块1–7。模块6读写角色文档并做关系演进与记忆回写；模块7嵌入技术参数。输出分行时间轴 + 每镜可复制 Prompt。 |

### 示意：深夜便利店（推介示例，非库内现成 demo）

**输入**：深夜便利店；你之前拒绝过的男生，顺手帮你捡起掉在地上的购物袋。人设：习惯自己扛事、怕欠人情、嘴硬心软；记忆里有一次对方递创口贴被自己拒了。

**人物创建侧会保住**：面具裂隙、记忆节点、关系人物——后续分镜必须贴档，禁止 OOC。

**叙事表演分镜侧会吐**：本场【空间关系】+ 时间轴 + 可复制 Prompt，例如表演行大致是——愣住、小声道谢不多说、接袋子时指尖尽量不碰、视线错开；台词短、语速偏快。

**回写**：本场若关系分寸有实质变化，记入记忆层，下次互动不漂。  
（库内开箱真 demo 是「周念白」档案 + 花墙拱门分镜，见 `references/`。）


## 联动三步

1. **人物创建**出标准人物文档（静态区锁定，动态区留空框架）  
2. **叙事表演分镜**导入该文档（模块6.1），分步确认后出分镜  
3. 用户确认事件定稿 → **模块6.2** 回写动态区（记忆追加、关系档位）；静态区只读

## 维护约定

- 准本：本机「人物创建 + 叙事表演剧本分镜 Skill（完整版）」。仓库 `skills/performance-coach/SKILL.md` 必须含标题 `### 模块6：角色文档读写与关系演进模块`。  
- **禁止**用 bot 现装精简版（只有模块1–4，约 38900 字节）覆盖 `skills/performance-coach/` 或把人物创建改回与模块6不对齐的旧档案模板。  
- `references/platform-adapter.md`、`references/demo-storyboard.md` 完整包里已有，保留。`references/demo-character.md`（周念白）按完整包原样保留，未改写。  

## 怎么安装

详见 [INSTALL.md](./INSTALL.md)。摘要：

```bash
cp -a skills/character-creator   <你的 agent-data/workflows>/character-creator
cp -a skills/performance-coach   <你的 agent-data/workflows>/performance-coach
```

无服务端、无 API Key、无 Docker。

## 触发语示例

**人物创建**：帮我创建一个角色 / 做角色档案 / 写人物小传  

**叙事表演剧本分镜**：写一段 AI 视频分镜 / 可灵表演 prompt / 双人戏分镜 / 启动叙事表演剧本分镜 skill  

## 示例与参考

[examples/README.md](./examples/README.md) → 各 skill `references/`（周念白、demo 分镜等）。

## 文件清单与发布

- [FILE-MANIFEST.md](./FILE-MANIFEST.md)  
- [RELEASE-CHECKLIST.md](./RELEASE-CHECKLIST.md)  
- [CHANGELOG.md](./CHANGELOG.md)  
- [docs/卖点详解.md](./docs/卖点详解.md)  

## 许可证

[MIT](./LICENSE) — Copyright (c) 2026 原  
主联系：yuan-ip@mail.grokbot.com  
抄送/备用：leonardy_2026@qq.com  
