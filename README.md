# Resume Maker - Claude Code Skill

一个 Claude Code 技能，帮你制作和定制简历。

## 描述

每次投简历都要重新调整内容？JD 里的关键词对不上？不同岗位侧重点不一样？Resume Maker 解决的就是这个问题。

核心思路：**全量母版 + 按岗位定制**。你的全部经历（教育、工作、项目、技能）一次性维护在母版里，每次投递只需告诉技能目标岗位和 JD，它会自动筛选最相关的内容、匹配关键词、调整描述侧重点，生成一份针对性的简历。

- 支持 Markdown / Word (.docx) / PDF 三种输出格式
- 项目经验遵循 STAR 法则，每个项目独立管理，带关键词标签和定制建议
- 首次使用引导式采集信息，之后更新简历一句话搞定

## 架构

```
resume-maker/
├── SKILL.md                    # 技能主指令
└── resources/
    ├── self_profile.md         # 你的背景、技能、求职偏好
    ├── resume_base.md          # 全量简历母版（所有经历）
    ├── project_template.md     # 项目文件模板（STAR法则）
    └── projects/
        ├── 项目A.md            # 每个项目独立维护
        └── 项目B.md
```

## 工作流程

1. **首次使用** → 技能引导你填写个人档案和经历母版
2. **每次投递** → 告诉技能目标岗位和 JD
3. **自动定制** → 从母版中筛选相关内容，匹配 JD 关键词
4. **生成输出** → 支持 Markdown / Word(.docx) / PDF

## 安装

将本仓库克隆到 Claude Code 的 skills 目录：

```bash
git clone https://github.com/AppleCG/resume-maker.git /path/to/.agents/skills/resume-maker
```

或者通过 Claude Code 的 skill 安装功能直接安装。

## 使用

在 Claude Code 中说：

- `帮我做一份简历` — 首次使用，采集信息
- `帮我把XX项目加到简历里` — 更新母版
- `帮我针对这个JD定制简历` — 粘贴JD，自动匹配
- `帮我生成一份英文简历` — 翻译并输出

## 定制原则

- **STAR 法则**：情境 → 任务 → 行动 → 结果，量化成果
- **关键词匹配**：JD 中的技能词自然融入简历
- **相关性排序**：最匹配的经历放最前面
- **一页优先**：5年以下经验控制在一页

## 贡献者

- [**AppleCG**](https://github.com/AppleCG) — 项目作者与维护者

欢迎提 Issue 和 PR。

## 许可

MIT License
