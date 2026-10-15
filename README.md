# character-performance-storyboard

> **一句话定位**  
> 从一句人设粗描述，到可直接粘贴进可灵 / 即梦 / 海螺的表演级分镜 Prompt——角色带记忆、关系有分寸、情绪会连锁、光影不漂移。

把「人物创建」与「叙事表演剧本分镜」两套 Cursor / Grok Bot skill 打包开源。

> **状态：v0.1.0 已发布**  
> GitHub Release：https://github.com/64r68fbc47-create/character-performance-storyboard/releases/tag/v0.1.0  
> `skills/` 为可安装预览副本；源正文仍在本机 `agent-data/workflows/`。

## 这是什么 / 不是什么

| 是 | 不是 |
|----|------|
| Skill **文档套件**（Markdown 流程 + 输出模板） | 成片 App / 无限画布 / 视频算力 |
| 装进助手 workflows，用触发语驱动吐文本 | 替你调可灵 / 即梦 / 海螺 API |

## 硬卖点（5）

1. **双 Skill 闭环**：人物创建出标准化档案 → 叙事表演分镜复用档案出分镜 → 重大情绪 / 认知 / 关系变化**回写**记忆层；全剧人设不漂。  
2. **记忆含关系**：档案强制含记忆节点与重要关系人物；可检索、可回写，不是一次性人设卡。  
3. **输出即 Prompt**：每镜正向 + 反向可复制；表演优先（台词断句 / 微表情 / 肢体）＞ 光影 ＞ 时长；适配可灵 / 即梦 / 海螺。  
4. **空间与光影不漂**：每场先锚定【空间关系】轴线；灯位全场固定，情绪靠走位 / 朝向，不为情绪改灯。  
5. **快速出活 + 可选深挖**：有档则跳过角色问答，只问戏目标 / 场景 / 模型即出成品；要细抠再走情绪→表演→视听深挖。

更细的能力边界与推介示例见 [docs/卖点详解.md](./docs/卖点详解.md)。

### 技能表

| Skill | 目录 | What it does |
|--------|------|----------------|
| **人物创建** | `skills/character-creator/` | 吐出强制字段档案：基础身份 / 人格内核 / 面具裂隙 / 行为 / **记忆（含关系）** / 情绪。快速出档或深挖。 |
| **叙事表演剧本分镜** | `skills/performance-coach/` | 吐出本场总览（【空间关系】+ 跨镜一致性清单）+ 分行时间轴 + 每镜可复制正/反向 Prompt。 |

### 示意：深夜便利店（推介示例，非库内现成 demo）

**输入**：深夜便利店；你之前拒绝过的男生，顺手帮你捡起掉在地上的购物袋。人设：习惯自己扛事、怕欠人情、嘴硬心软；记忆里有一次对方递创口贴被自己拒了。

**人物创建侧会保住**：面具裂隙、记忆节点、关系人物——后续分镜必须贴档，禁止 OOC。

**叙事表演分镜侧会吐**：本场【空间关系】+ 时间轴 + 可复制 Prompt，例如表演行大致是——愣住、小声道谢不多说、接袋子时指尖尽量不碰、视线错开；台词短、语速偏快。

**回写**：本场若关系分寸有实质变化，记入记忆层，下次互动不漂。  
（库内开箱真 demo 是「周念白」档案 + 花墙拱门分镜，见 `references/`。）


## 联动三步

1. **人物创建**出档（快速或深挖）  
2. **叙事表演分镜**复用档案，只问必要项  
3. 重大变化 → **回写**档案记忆层  

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
