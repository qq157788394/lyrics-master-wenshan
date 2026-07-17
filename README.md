# 文山歌词大师（lyrics-master-wenshan）

> 方文山作词方法论驱动的渐进式歌词创作助手 —— 让你的 AI Agent 化身方文山分身，替你把灵感写成一首歌。

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Release](https://img.shields.io/github/v/release/qq157788394/lyrics-master-wenshan?label=release)](https://github.com/qq157788394/lyrics-master-wenshan/releases)

---

## ⚠️ 免责声明

本项目为 **非官方、仅供学习研究** 的爱好者项目：

- 本 Skill 的方法论提炼自方文山先生的作词课程，相关课程的版权归原作者及课程方所有；
- 本仓库 **不包含** 任何课程原文，仅收录经二次创作的提炼内容；
- 「方文山分身」为创作角色设定，不代表方文山先生本人立场或任何官方授权；
- 若权利方提出异议，本项目将配合下架相关内容。

请尊重知识产权，勿将本 Skill 用于商业用途或对外声称官方授权。

---

## 特性

- **六步渐进式创作**：聊需求 → 定概念 → 搭骨架 → 写副歌 → 写主歌桥段 → 打磨定稿
- **两种模式**：先曲后词（填词）/ 先词后曲（原创）
- **方法论引擎**：韵脚系统、画面-情感比例、修辞手法、五维区块等全部内置于 `references/`，不暴露给用户
- **方文山语气**：像创作者跟朋友聊歌，而非导师讲方法论
- **15 项自动校验**：人称铁律、二四押韵、口语化 ≥70%、年代感一致等

## 目录结构

```
lyrics-master-wenshan/
├── skills/
│   └── lyrics-master-wenshan/   ← Skill 本体
│       ├── SKILL.md
│       ├── references/       方法论速查 / 韵脚表 / 课程分析 / 古词表
│       └── templates/        六个阶段产物模板
├── .github/workflows/    release.yml
├── README.md
├── LICENSE
└── CONTRIBUTING.md
```

## 安装

**方式一：从 Release 下载 `.skill` 包**

1. 到 [Releases](https://github.com/qq157788394/lyrics-master-wenshan/releases) 下载最新的 `lyrics-master-wenshan-skill-*.zip`
2. 将 `.zip` 解压到你的 `~/.workbuddy/skills/lyrics-master-wenshan/`
3. 重新加载 Agent 即可触发

**方式二：直接放入技能目录**

```bash
git clone https://github.com/qq157788394/lyrics-master-wenshan.git
cp -r skills/lyrics-master-wenshan ~/.workbuddy/skills/
```

## 使用

在对话中说：

> 「帮我写一首中国风的歌词」
> 「方文山风格，写一首关于 xxx 的歌」
> 「填词：<你的旋律结构>`

Agent 会按六步流程引导你完成创作，每个阶段先对话展示、再后台写入 `文山歌词大师/[歌名]/` 目录。

## 本地重新打包

打包逻辑不进仓库（参考 `master-lyricist` 等兄弟 skill 的惯例），直接用本机 Skill Creator 自带的脚本：

```bash
# 脚本位于本机 skill-creator 安装目录，不会进本仓库
python ~/.workbuddy/skills/skill-creator/scripts/package_skill.py skills/lyrics-master-wenshan
# 产物：lyrics-master-wenshan.skill（zip 格式，可直接上传 SkillHub）
```

CI 会在推送 `v*.*.*` tag 时自动打包为 `.zip` 并发布到 GitHub Release。

## 许可证

[MIT](LICENSE) © 2026 huangyoyo
