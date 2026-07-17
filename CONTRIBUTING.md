# 贡献指南

感谢你有兴趣让「文山歌词大师」变得更好！

## 提交流程

1. Fork 本仓库并 `git clone` 到本地
2. 基于 `main` 创建特性分支：`git checkout -b feat/your-change`
3. 修改 `.workbuddy/skills/lyrics-master-wenshan/` 下的内容
4. 本地校验：
   ```bash
   pip install pyyaml
   python tools/package_skill.py .workbuddy/skills/lyrics-master-wenshan dist
   ```
   若校验失败，请先修复再提交
5. 提交并推送到你的 Fork，发起 Pull Request 到 `main`

## 规范

- Skill 本体只放 Agent 执行所需的文件，勿将 README / CHANGELOG 等辅助文档放进 skill 目录
- 修改 `SKILL.md` 后，请确保 frontmatter 的 `name` 保持 hyphen-case、`description` 清楚描述触发场景
- 提交信息建议遵循 Conventional Commits（如 `feat:`、`fix:`、`docs:`）
- 请勿将课程原文（`方文山作词课程_导出/`）或用户作品纳入提交

## 行为准则

请文明、友善地交流。本仓库采用 [Contributor Covenant](CODE_OF_CONDUCT.md) 行为准则。
