# 1-plan.md

## Goals
- Automate repetitive Mac tasks for internal use.
- Provide a modular, extensible workflow runner.
- Save time, reduce errors, and allow easy addition of new tasks.

## Scope
**In scope:** Mac task automation via code workflows, CLI, basic logging.  
**Out of scope:** GUI, cross-platform support, advanced AI, cloud integration.

## Feature Priorities (MoSCoW)
- **Must:** Workflow engine, initial task library, config-based workflows, CLI, logging.
- **Should:** Scheduling, error notifications, plugin system.
- **Could:** Simple GUI, ML suggestions, cross-platform.
- **Won’t:** Cloud service integration, full NLP interface.

## Milestones
1. **MVP** – Engine, sample workflows, CLI, logging.
2. **Library & Scheduling** – More tasks, scheduling support.
3. **Plugin Architecture** – Add tasks without core changes.
4. **Polish & Beta** – Error handling, notifications, feedback.

## Success Criteria
- Automate ≥5 major workflows.
- Save ~50% manual time on targeted processes.
- ≥95% workflow success rate over 1 month.
- Add new tasks in <1 day.
- Positive internal feedback.

## Risks & Mitigation
- **Scope creep:** Enforce in/out scope list, backlog new ideas.
- **macOS dependency:** Use stable APIs, monitor OS updates.
- **Solo dev risk:** Document, use version control.
- **Unclear requirements:** Set measurable goals, get feedback.
- **Tech debt:** Refactor regularly, keep code modular.

## Evolution Strategy
- Grow incrementally via backlog.
- Modular design for easy changes.
- Refactor regularly to avoid debt.
- Keep docs updated as a living reference.
