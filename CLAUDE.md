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

**samurai task-board** — タスク管理ボードアプリケーション。

- **リポジトリ:** https://github.com/anpan-jampan/task-board
- **公開URL:** https://anpan-jampan.github.io/task-board/

## 技術スタック

- **React 18** — UIフレームワーク（関数コンポーネント + Hooks）
- **Vite 6** — ビルドツール・開発サーバー
- **localStorage** — タスクの永続化（キー: `task-board-tasks`）
- **GitHub Actions** — `master` へのプッシュ時に自動ビルド＆GitHub Pagesへデプロイ

### 主要コマンド

```bash
npm run dev      # 開発サーバー起動 (http://localhost:5173)
npm run build    # プロダクションビルド → dist/
```

## 命名規約

- **コンポーネントファイル:** PascalCase（例: `TaskList.jsx`、`AddTaskForm.jsx`）
- **コンポーネント関数:** PascalCase（例: `export default function TaskList()`）
- **CSSクラス名:** kebab-case（例: `.task-list`、`.delete-btn`）
- **状態・変数:** camelCase（例: `tasks`、`inputValue`）
- **定数:** UPPER_SNAKE_CASE（例: `STORAGE_KEY`）
