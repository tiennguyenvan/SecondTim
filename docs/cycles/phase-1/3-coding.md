# 3-coding.md

## Sprint Plan (Phase 1)

### Sprint 1 – Core MVP Setup (2 weeks)
**Goals:**
- Create repo, project structure, and initial CLI.
- Implement Workflow Engine skeleton.
- Add logging module.
- Implement 1–2 simple block modules.

**Backlog:**
- [v] Create repo and folder structure (`engine/`, `blocks/`, `workflows/`, `cli/`, `logs/`).
- [ ] Setup CLI entry point (`secondtim run <workflow>`).
- [ ] Implement Engine to load YAML workflow and sequentially run blocks.
- [ ] Add centralized logging (stdout + file).
- [ ] Implement sample blocks:  
  - Launch an app.  
  - Move files between folders.
- [ ] Write example YAML workflow and run it end-to-end.
- [ ] Commit and tag as `v0.1`.

---

### Sprint 2 – Block Library Expansion & Config Improvements (2 weeks)
**Goals:**
- Add more built-in block modules.
- Improve config parsing and validation.
- Pass data between blocks.

**Backlog:**
- [ ] Implement 3–5 more blocks (e.g., copy files, rename files, open URL, send email via AppleScript, run shell command).
- [ ] Add input/output data passing between blocks in Engine.
- [ ] Add workflow config validation (schema check).
- [ ] Allow parameters in workflow config (YAML placeholders).
- [ ] Update docs with new blocks and config format.
- [ ] Write tests for Engine and at least 3 blocks.

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
- Refactor Engine to dynamically load block modules.
- Document how to add new blocks.

**Backlog:**
- [ ] Implement dynamic block discovery (scan `blocks/` dir).
- [ ] Define `BlockInterface` and enforce it for all modules.
- [ ] Refactor existing blocks to match interface.
- [ ] Add example “external” block to prove plugin loading works.
- [ ] Write `ADDING_BLOCKS.md` guide.
- [ ] Tag as `v1.0` – Phase 1 complete.

---

## Notes
- Keep sprints tight and achievable (solo dev = 1–2 weeks per sprint).
- Always leave time at end of sprint for refactoring & doc updates.
- Backlog items can move between sprints if blocked.
- Post-Phase 1, proceed to `4-deploy.md` and `5-maintain.md` for rollout and upkeep.
