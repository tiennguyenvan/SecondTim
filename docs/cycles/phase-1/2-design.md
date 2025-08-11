# 2-design.md

## Overview
- Modular monolith CLI tool for macOS automation.
- Event-driven workflow engine triggers task modules.
- Principles: separation of concerns, extensibility, fail-safe, minimal coupling.

## Components
- **Workflow Engine:** Orchestrates tasks, passes data, handles errors.
- **Task Modules:** Independent scripts/classes for specific automations.
- **Workflow Definitions:** YAML/config to list tasks and params.
- **Scheduler (optional):** Triggers workflows on schedule.
- **Logging:** Centralized logs for runs and errors.
- **CLI Interface:** Run workflows, list available ones.

## Data & Control Flow
1. Trigger (CLI/Scheduler).
2. Engine loads workflow definition.
3. Engine runs each task module in order, passing outputs.
4. Logs every step; stops or continues based on errors.
5. Final log/notifications.

## Extensibility
- Plugin-like tasks discovered dynamically.
- Config-driven workflows (no core code changes).
- Loose coupling for easy swaps/replacements.

## Interface Contracts
- **Task Module:** `execute(context) -> result` or raise `TaskError`.
- **Engine/Scheduler:** Common `run_workflow(name)` entry point.
- **Config Format:** Defined YAML/JSON structure for workflows.
- **Error Handling:** Exceptions logged, workflow halts by default.

## Tech Stack
- **Language:** Python 3.11 for speed of dev + macOS libs.
- **Automation:** AppleScript (osascript), PyObjC, shell commands.
- **CLI:** Click or argparse.
- **Storage:** Filesystem for configs/logs (SQLite later if needed).
- **Tools:** Git, pytest, flake8/black.

## Key Decisions
- Modular monolith over microservices (simplicity).
- YAML for workflow definitions (readable, safe).
- AppleScript for app control, Python/shell for system tasks.
- Fail-fast error strategy (transparent, simple).

## Maintainability
- Modular code, regular refactoring.
- Living documentation.
- Basic tests for critical parts.
- Backlog-driven iterative growth.
