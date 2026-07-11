# Zlong Marp Skill

[中文](#中文) | [English](#english)

## 中文

`zlong-marp` 是一个以鲜明个人风格生成 Marp 幻灯片的 Agent Skill，主要面向科研汇报与组会演示。它可以读取提示词、附件、独立大纲文件或已有 Marp Markdown 中的内容，并应用内置的版式、语义配色、数学排版和可视化规范。

### VS Code、Marp 插件与 HTML 设置

推荐在 VS Code 中安装由 Marp Team 发布的 **Marp for VS Code** 插件，用于实时预览和导出。

该模板大量使用 HTML 和 CSS 布局。请在 VS Code 设置中找到 `Markdown › Marp: HTML`，并将其设置为 `all`。对应的工作区设置为：

```json
{
  "markdown.marp.html": "all"
}
```

VS Code 工作区还必须处于受信任状态。未受信任的工作区会将该选项始终视为 `off`，导致模板中的 HTML 布局无法正常渲染。

### 安装到 Agent

#### GitHub Copilot（VS Code）

项目级 Skill 可放在目标仓库的以下任一位置：

```text
.github/skills/zlong-marp
.agents/skills/zlong-marp
```

个人级 Skill 可放在：

```text
~/.copilot/skills/zlong-marp
~/.agents/skills/zlong-marp
```

随后在 Copilot Chat 的 Agent 模式中明确要求使用 `zlong-marp`。Skill 也可以在请求与其描述匹配时被自动选择；具体显式调用方式取决于当前 Copilot 版本。

#### Codex

将完整的 `zlong-marp` 目录放在：

```text
$CODEX_HOME/skills/zlong-marp
```

如果没有单独设置 `CODEX_HOME`，通常使用：

```text
~/.codex/skills/zlong-marp
```

重新启动 Codex 或新建任务后，可以通过 `$zlong-marp` 显式调用。

#### Claude Code

项目级 Skill 放在目标仓库的：

```text
.claude/skills/zlong-marp
```

个人级 Skill 放在：

```text
~/.claude/skills/zlong-marp
```

Claude Code 可以根据描述自动选择该 Skill，也可以通过 `/zlong-marp` 显式调用。首次创建顶层 Skill 目录后，如果当前会话没有检测到它，请重新启动 Claude Code。

### 推荐工作流

1. 为本次汇报创建一个单独的文件夹。
2. 在其中创建 `slide.md`，并粘贴大纲和已有材料。
3. 让 Agent 使用 `zlong-marp`，直接完善当前的 `slide.md`。
4. 手动检查和微调生成结果。
5. 在 VS Code 中预览，并在完成调整后手动导出。

这是推荐的个人工作流，而不是 Skill 的输入限制。也可以直接在提示词中提供大纲，使用附件或其他文件名，并指定不同的 Marp Markdown 输出位置。

示例提示词：

```text
Use $zlong-marp to turn the outline in slide.md into a complete Marp presentation.
Edit slide.md in place. Do not export it yet.
```

## English

`zlong-marp` is an Agent Skill for generating Marp slides with a distinctive personal style, primarily for research presentations and group meetings. It can read content from a request, attachment, separate outline file, or existing Marp Markdown source and apply its bundled layout, semantic-color, mathematical-typesetting, and visualization conventions.

### VS Code, Marp extension, and HTML setting

Install the **Marp for VS Code** extension published by the Marp Team for live preview and export.

The template relies heavily on HTML and CSS layouts. In VS Code settings, find `Markdown › Marp: HTML` and set it to `all`. The equivalent workspace setting is:

```json
{
  "markdown.marp.html": "all"
}
```

The VS Code workspace must also be trusted. In an untrusted workspace, this option is always treated as `off`, so the template's HTML layouts will not render correctly.

### Agent installation

#### GitHub Copilot in VS Code

Place a project Skill in either location within the target repository:

```text
.github/skills/zlong-marp
.agents/skills/zlong-marp
```

Place a personal Skill in either:

```text
~/.copilot/skills/zlong-marp
~/.agents/skills/zlong-marp
```

Then explicitly ask Copilot Chat in Agent mode to use `zlong-marp`. Copilot may also select the Skill automatically when the request matches its description; the available explicit invocation syntax depends on the installed Copilot version.

#### Codex

Place the complete `zlong-marp` directory in:

```text
$CODEX_HOME/skills/zlong-marp
```

When `CODEX_HOME` is not configured separately, the usual location is:

```text
~/.codex/skills/zlong-marp
```

Restart Codex or start a new task, then invoke the Skill explicitly with `$zlong-marp`.

#### Claude Code

Place a project Skill in:

```text
.claude/skills/zlong-marp
```

Place a personal Skill in:

```text
~/.claude/skills/zlong-marp
```

Claude Code can select the Skill automatically from its description or invoke it explicitly with `/zlong-marp`. If a newly created top-level Skill directory is not detected in the current session, restart Claude Code.

### Recommended workflow

1. Create a dedicated folder for the presentation.
2. Create `slide.md` inside it and paste in the outline and available material.
3. Ask an Agent to use `zlong-marp` and complete the current `slide.md` in place.
4. Review and refine the generated source manually.
5. Preview it in VS Code and export it manually after refinement.

This is the recommended personal workflow, not an input restriction. The outline may instead be supplied directly in the request, attached, stored under another filename, or written to a different Marp Markdown target.

Example prompt:

```text
Use $zlong-marp to turn the outline in slide.md into a complete Marp presentation.
Edit slide.md in place. Do not export it yet.
```

## 仓库结构 / Repository structure

```text
ZlongMarpSkill/
├── .gitignore
├── README.md
└── zlong-marp/
    ├── SKILL.md
    ├── agents/
    ├── assets/
    └── references/
```
