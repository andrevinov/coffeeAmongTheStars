# Documentation guide

This guide explains where to find information about Coffee Among the Stars and where new documentation belongs. It describes the agreed documentation structure; a listed document or module does not necessarily exist yet.

## Start here

- [README](../README.md) is the entry point. It gives a short view of the game, its goals, its current status, and the technical direction.
- [AGENTS.md](../AGENTS.md) explains how development proceeds, including the rule of one understood conceptual unit at a time.
- This guide explains how the other documents relate to those entry points.

## Documents to add as their subjects become real

| Location | Purpose |
| --- | --- |
| `docs/ubiquitous-language.md` | Define agreed game terms so they mean the same thing across discussions, code, and documentation. It is a reference alongside the README, not a deeper layer of it. |
| `docs/how-it-works.md` | Explain the game's implemented behavior at a high level: module responsibilities, their interactions, and the relevant dependency direction. It expands on the README without becoming a catalogue of classes. |
| `docs/modules/<module>.md` | Explain one existing module's responsibility, internal flow, and important boundaries. Mention its constituent concepts briefly and link to their detailed explanations where useful. |
| `docs/concepts/<module>/<concept>.md` | Explain one existing class or function when it needs more than a short description in code: its role, behavior, methods when applicable, and relevant design decisions. |
| `docs/roadmap.md` | Record milestones and revisable hypotheses about future work. Planned behavior belongs here rather than in descriptions of implemented software. |

These paths are an organizational direction, not a list of files to create in advance. Names and grouping can change when the software gives us a reason to change them.

## Keep each level distinct

The README answers **what the project is**. `how-it-works.md` answers **how the implemented parts work together**. A module document answers **what one module owns and how its parts cooperate**. A concept document answers **how one class or function behaves**. The glossary can be consulted from any level.

Module documents should not repeat method-level explanations from concept documents. A concept document should not repeat the module's full interaction map. A simple class or function may need only a docstring rather than a separate document.

A module is a cohesive responsibility of the game; it is not automatically a Clean Architecture layer. When a layer or dependency boundary matters, explain it in the document where that decision can be understood.

Describe implemented behavior as implemented behavior, and label future ideas as plans. Add documentation for one understood concept at a time, as described in [AGENTS.md](../AGENTS.md).
