# kenton-link-lens Quickstart

本指南用于完成一次最短的首次成功：让 Agent 发现 `kenton-link-lens`，读取一个可访问链接，并按三阶段结构交付结果。

## 1. 确认宿主条件

你的 Agent 宿主需要：

- 支持从目录加载 `SKILL.md`；
- 能在新会话中显示或调用名为 `kenton-link-lens` 的 Skill；
- 具备访问目标 URL 所需的浏览器、网络或文件读取能力。

本项目没有声明兼容的宿主名称和版本。请以宿主官方文档中的 Skills 目录与刷新方式为准。

## 2. 安装 Skill

```bash
git clone https://github.com/JefferyMaa/kenton-link-lens.git
cp -R kenton-link-lens <YOUR_AGENT_SKILLS_DIR>/
```

不要把 `<YOUR_AGENT_SKILLS_DIR>` 原样执行；它代表宿主要求的 Skills 目录。

安装后重新启动宿主或开启新会话，检查可用 Skill 列表中是否出现：

```text
kenton-link-lens
```

## 3. 选择首次测试链接

第一次测试优先选择：

- 无需登录；
- 页面较短但内容完整；
- 你有权访问和分析；
- 不需要下载大文件。

这样可以先验证 Skill 发现与输出结构，再测试 GitHub 仓库、长视频或受限网页。

## 4. 发送测试请求

```text
帮我用 kenton-link-lens 深挖这个：<URL>
```

若你希望检查仓库，可进一步明确：

```text
用 kenton-link-lens 吃透这个仓库。先说明你实际读取了哪些文件，再拆架构、判断成色，并给出采用方案：<GITHUB_REPOSITORY_URL>
```

## 5. 验收结果

首次成功不以“Agent 回复了”作为标准。结果至少应证明：

1. Agent 说明实际读到的内容和证据缺口；
2. 对象被拆成多个具体组成部分；
3. 有独立判断，而不是复述作者自述；
4. 有想法、方案或下一步行动；
5. 没有把存档、内容生产或变现当成默认终点。

若缺少其中任一项，见 [故障排查](troubleshooting.md)。

## 6. 再测试复杂输入

基础测试通过后，再逐步尝试：

- GitHub 仓库：要求读取核心代码、配置、测试与 issue 证据；
- 长文章：要求覆盖完整论证和反例；
- 视频：先确认下载体积、磁盘位置和转写能力；
- 登录内容：只在你明确授权且宿主具备安全会话能力时处理。

复杂输入的成功标准仍然是“证据充分的完整分析”，不是下载或转写动作本身。
