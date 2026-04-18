# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Git Workflow

**Push to GitHub after every code change.**

```bash
git add <changed-files>
git commit -m "concise description of change"
git push
```

- Stage specific files by name — never use `git add -A` or `git add .` blindly.
- Commit messages should describe *why*, not just *what*.
- After every meaningful code change (new feature, bug fix, refactor), push immediately to keep the remote up to date.
- If the remote branch does not exist yet, use `git push -u origin <branch>`.

## Project

This is **samurai task-board** — a task management board application. Architecture and commands will be documented here as the project is built out.
