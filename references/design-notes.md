# Design Notes

## Core Idea

OpenWhip explores a simple question:

> What if waiting for an AI response had a playful feedback button?

AI tools often leave users staring at a screen while the system thinks, runs code, or appears stuck. The interaction is usually passive. OpenWhip adds a safe, visible outlet: a colored whip animation and a short phrase that expresses the user's desired state.

## Why A Visual Nudge

The goal is not to control the model. The goal is to make waiting feel less blank.

A visual nudge works because it:

- gives the user something intentional to do,
- makes the current mood visible,
- creates a memorable demo moment,
- keeps the interaction lightweight and reversible.

## Color Logic

Each color represents a stage in a small workflow story:

| Color | State | Meaning |
| --- | --- | --- |
| Red | Wake up | Start the nudge |
| Orange | Nudge | Ask for more speed |
| Yellow | Speed up | Raise urgency |
| Blue | Unstick | Recover from perceived stalling |
| Green | Work mode | Continue execution |
| Purple | Review | Finish and inspect |

## Why Not Interrupt The Task

Interrupting an AI or terminal process can be risky. It may cancel useful work, corrupt a workflow, or create confusing side effects.

OpenWhip intentionally avoids that. It does not send interrupt keys, type into active windows, or manipulate running tasks. The interaction is purely a feedback layer.

## Extensibility

The same pattern can be adapted to other visual metaphors:

- a conductor baton for orchestration,
- a progress spirit for long-running tasks,
- a status badge for agent phases,
- a tiny dashboard for local workflow states.

Future versions could respond to real task events if an AI tool exposes official state APIs.
