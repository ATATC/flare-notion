# FLARE Notion

A reusable Codex skill for maintaining the FLARE lab's Notion projects and Master Tasks.

## Rules

1. Every task requires **Category, Owner, Priority, Stage, Expected time (h), and Time required**.
2. Calibrate estimates using actual durations from comparable completed work.
3. Record actual time when completing a task. Ask for the duration if it is unknown; never substitute an estimate for an actual.
4. Every actionable step, however small, is a **top-level Master Task**. Keep `Parent task` empty and link each task to its project. Do not hide actionable steps in another task's body.

The skill also keeps planning estimates separate from actual effort, checks for duplicates, and verifies saved properties.

## Install in Codex

Paste this into Codex:

```text
Use $skill-installer to install the flare-notion skill from https://github.com/ATATC/flare-notion/tree/main/skills/flare-notion
```

The installer places the skill in your personal skills directory (`$CODEX_HOME/skills`, or `~/.codex/skills` by default). It will be available on your next turn. If a copy is already installed, ask Codex to update that copy from this repository instead of creating a duplicate.

## Use

```text
Use $flare-notion to maintain the tasks for FLARE T3 Summary Paper. Fill missing required fields and calibrate unfinished-task estimates from completed work.
```

```text
Use $flare-notion to mark my method-review task completed. It took 1 hour.
```

```text
Use $flare-notion to break this project plan into separate top-level Master Tasks, with owners, priorities, and calibrated effort estimates.
```

Provide the target project and assignee when they are not clear from context. The skill supports automatic selection for relevant Notion task requests as well as explicit invocation.

## Access and workspace

You need access to the lab's Notion workspace and a supported computer-use session in the Notion desktop app or browser. This skill uses the visible Notion UI exclusively; it does not use Notion MCP connectors or direct Notion API access. Installing the skill supplies instructions; it does not grant Notion access or install computer-use tools.

The skill links to the lab's existing Master Tasks database and FLARE T3 Summary Paper project. Those pages retain their existing Notion permissions. It uses the project specified in your request and identifies the current task owner rather than defaulting to the repository author.

For a different workspace, adapt the workspace links and property mappings in your local copy. Preserve the four rules above, and check the current schema before making edits.

## Files and maintenance

- [`skills/flare-notion/SKILL.md`](skills/flare-notion/SKILL.md): workflow and field rules.
- [`skills/flare-notion/agents/openai.yaml`](skills/flare-notion/agents/openai.yaml): Codex display and invocation metadata.

The package contains instructions only: no credentials or executable automation. Keep personal task logs and credentials out of this repository. Calibration should use live, authorized Notion records rather than treating the historical example in the skill as a fixed estimate.
