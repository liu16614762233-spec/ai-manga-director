# AI Manga Director

AI Manga Director 是一个通用智能体工作流包，用于把剧本转成可执行的 AI 漫剧、AI 短剧和电影感图生视频制作流程。

它不是提示词合集，而是一套生产系统：剧本、项目事实、资产门禁、导演调度、控制图判断、Seedance 风格视频提示词、声音设计、审片和返工。

## 它解决什么问题

很多 AI 视频失败，不是模型完全不行，而是流程直接从“剧情说明”跳到了“视频 Prompt”。中间缺少导演和制片环节。

这个包补上了这些环节：

- **先过门禁再生成**：主角、场景、道具、台词、时间可执行性没确认，不直接写正式视频 Prompt。
- **先做导演调度预演**：明确摄影机、景别、动作、焦点、转场、结尾停点，而不是写剧情梗概。
- **反推最少必要资产**：判断本轮到底需要哪些角色图、场景图、道具图、控制图，不机械补全所有图。
- **适配 Seedance 2.0 全能参考逻辑**：每张参考图必须说明负责什么、不负责什么。
- **默认角色定妆标准**：主角/主要角色第一次出图默认是 9:16 不等大四格专业角色定妆参考板，不被三视图、多视图误替代。
- **声音和台词进入流程**：原剧本台词、声音一致性、环境音、拟音、无背景音乐素材生成规则都要检查。
- **保留样片返工**：审片后优先保留原本可用画面，只修最高风险问题，不随便重写成另一个片段。

## 适合谁

- AI 漫剧创作者
- AI 短剧 / 电影感短片创作者
- 使用 Seedance、Runway、Kling、Veo、即梦等图生视频工具的人
- 需要长期连续性和资产管理的项目
- 想把 Custom GPT / Claude / Codex / 本地 Agent 做成制作助手的人

## 文件怎么用

如果你的平台支持上传知识库或项目文件：

1. 上传 `skills/ai-manga-director/SKILL.md`
2. 上传 `skills/ai-manga-director/references/` 里的全部文件
3. 可选上传 `UNIVERSAL_AGENT_PROMPT.md` 作为启动指令

如果你的平台只支持粘贴指令：

1. 复制 `UNIVERSAL_AGENT_PROMPT.md`
2. 粘贴到系统指令 / 项目指令 / 自定义助手指令
3. 根据需要再把 references 里的对应文件上传或粘贴

## 推荐第一句话

```text
Use AI Manga Director in compact mode. First identify my task type, current gate, missing required assets, and the next allowed action. Do not write a final video prompt until gates pass.
```

中文也可以：

```text
使用 AI Manga Director，进入简洁模式。先判断任务类型、当前门禁、缺失资产和下一步允许动作；门禁未通过前不要写正式视频 Prompt。
```

## 典型流程

```text
剧本
→ 剧本移交制作检查
→ 项目事实确认
→ 主要角色 / 必要场景 / 关键道具门禁
→ 导演调度预演
→ 资产反推
→ 控制图判断
→ 出图 / 审图 / 精修
→ 视频 Prompt
→ 审片
→ 保留样片返工
```

## 快速体验

查看：

- `docs/quickstart.md`
- `examples/mini-project/`

这两个文件可以直接作为最小上手案例。
