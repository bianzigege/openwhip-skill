---
name: openwhip-skill
description: Trigger or describe OpenWhip-style visual feedback when the user says phrases like 抽一下, 甩一下, whip, 快一点, 再快一点, 加速, 别卡了, 醒醒, 干活, 工作, 检查一下, 检查, or review. Use this skill to map user intent to a safe visual nudge, not to interrupt or control running tasks.
---

# OpenWhip Skill

Use this skill when the user wants to trigger, describe, or script OpenWhip-style visual feedback for an AI workflow.

## Intent

OpenWhip turns waiting-state frustration into a lightweight visual cue. It may trigger a local visual controller when one is available, or simply respond with the mapped phrase when no controller is configured.

## Action Mapping

| User phrase | Action | Color | Response phrase |
| --- | --- | --- | --- |
| `抽一下`, `甩一下`, `whip` | `waving` | `red` | 第一鞭，先醒醒，别让我干等。 |
| `快一点` | `waving` | `orange` | 快一点，别让我在这儿干等。 |
| `再快一点`, `冲刺` | `waving` | `yellow` | 再快一点，节奏拉起来。 |
| `别卡了`, `醒醒` | `waiting` | `blue` | 别卡住，往前冲。 |
| `干活`, `工作` | `running` | `green` | 干活干活，别偷懒。 |
| `检查一下`, `检查`, `review` | `review` | `purple` | 最后检查一遍，收工别漏东西。 |

## Runtime Behavior

If a local OpenWhip trigger command is configured in the user environment, invoke it with the closest keyword. If no trigger command is available, do not invent one. Reply with the mapped phrase and optionally explain which visual action it represents.

Keep responses short. The expected UX is quick feedback, not a long explanation.

## Safety Rules

- Do not send `Ctrl-C`, `Esc`, or any other interrupt key.
- Do not type commands into terminals or editors.
- Do not claim that this actually speeds up the AI model.
- Do not read private chat content, browser data, account data, tokens, logs, or local runtime files.
- Treat OpenWhip as a visual feedback layer only.

## Suggested Demo Order

Use the left-to-right keyboard story:

1. `Option + A`: wake up
2. `Option + S`: nudge
3. `Option + D`: speed up
4. `Option + F`: unstick
5. `Option + G`: work mode
6. `Option + H`: review
