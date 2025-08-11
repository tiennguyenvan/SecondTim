# 3-coding.md

## Sprint Plan (Phase 1)

### Sprint 1 – Core MVP Setup (2 weeks)
**Goals:**
- Create repo, project structure, and initial CLI.
- Implement Workflow Engine skeleton.
- Add logging module.
- Implement 1–2 simple task modules.

**Backlog:**
- [ ] Create repo and folder structure (`engine/`, `tasks/`, `workflows/`, `cli/`, `logs/`).
- [ ] Setup CLI entry point (`secondtim run <workflow>`).
- [ ] Implement Engine to load YAML workflow and sequentially run tasks.
- [ ] Add centralized logging (stdout + file).
- [ ] Implement sample tasks:  
  - Launch an app.  
  - Move files between folders.
- [ ] Write example YAML workflow and run it end-to-end.
- [ ] Commit and tag as `v0.1`.

---

### Sprint 2 – Task Library Expansion & Config Improvements (2 weeks)
**Goals:**
- Add more built-in task modules.
- Improve config parsing and validation.
- Pass data between tasks.

**Backlog:**
- [ ] Implement 3–5 more tasks (e.g., copy files, rename files, open URL, send email via AppleScript, run shell command).
- [ ] Add input/output data passing between tasks in Engine.
- [ ] Add workflow config validation (schema check).
- [ ] Allow parameters in workflow config (YAML placeholders).
- [ ] Update docs with new tasks and config format.
- [ ] Write tests for Engine and at least 3 tasks.

---

### Sprint 3 – Scheduling & Notifications (2 weeks)
**Goals:**
- Enable workflows to be triggered on a schedule.
- Add basic error notifications.

**Backlog:**
- [ ] Implement schedule support (macOS `launchd` job or built-in Python scheduler).
- [ ] Add workflow trigger type in config (manual vs scheduled).
- [ ] Implement simple notification (macOS notification center or email).
- [ ] Add logging of trigger source (CLI or scheduler).
- [ ] Test scheduled workflows and notifications.
- [ ] Update CLI to list upcoming scheduled workflows.

---

### Sprint 4 – Plugin Architecture & Extensibility (2 weeks)
**Goals:**
- Refactor Engine to dynamically load task modules.
- Document how to add new tasks.

**Backlog:**
- [ ] Implement dynamic task discovery (scan `tasks/` dir).
- [ ] Define `TaskInterface` and enforce it for all modules.
- [ ] Refactor existing tasks to match interface.
- [ ] Add example “external” task to prove plugin loading works.
- [ ] Write `ADDING_TASKS.md` guide.
- [ ] Tag as `v1.0` – Phase 1 complete.

---

## Notes
- Keep sprints tight and achievable (solo dev = 1–2 weeks per sprint).
- Always leave time at end of sprint for refactoring & doc updates.
- Backlog items can move between sprints if blocked.
- Post-Phase 1, proceed to `4-deploy.md` and `5-maintain.md` for rollout and upkeep.
